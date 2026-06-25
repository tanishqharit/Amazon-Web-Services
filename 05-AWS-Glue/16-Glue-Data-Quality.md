# Glue Data Quality

## What is Glue Data Quality?

**Glue Data Quality** lets you define **rules** to validate your data — checking for completeness, correctness, and consistency.

---

## Why Data Quality Matters

Bad data = bad decisions. Common problems:
- Missing values (null names, empty fields)
- Duplicates (same order counted twice)
- Invalid values (age = -5, date = "abc")
- Late data (yesterday's data arriving today)

---

## How It Works

You write rules using **DQDL (Data Quality Definition Language)**:

```
Rules = [
    ColumnExists "customer_id",
    Completeness "customer_id" > 0.95,
    Uniqueness "order_id" > 0.99,
    ColumnValues "age" between 0 and 150
]
```

---

## Common Rules

| Rule | What it checks |
|------|---------------|
| `Completeness` | % of non-null values |
| `Uniqueness` | % of unique values |
| `ColumnExists` | Column is present |
| `ColumnValues` | Values within expected range |
| `RowCount` | Number of rows meets expectation |
| `DataType` | Values match expected type |

---

## What Happens When Rules Fail?

You can configure:
- **Fail the job** — stop processing bad data
- **Log warnings** — continue but alert you
- **Quarantine bad data** — send bad records to a separate location

---

## Key Takeaway

> Glue Data Quality validates data using declarative rules. Check for completeness, uniqueness, and valid ranges. Use it to prevent bad data from entering your data lake.

---

**Previous:** [Glue Connections](./15-Glue-Connections.md)
**Next:** [Glue Schema Registry](./17-Glue-Schema-Registry.md)

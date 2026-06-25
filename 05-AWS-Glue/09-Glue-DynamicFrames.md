# Glue DynamicFrames

## What is a DynamicFrame?

A **DynamicFrame** is Glue's own data structure — similar to a Spark DataFrame but with extra features for handling messy data.

---

## DynamicFrame vs Spark DataFrame

| Feature | DynamicFrame | Spark DataFrame |
|---------|-------------|-----------------|
| **Schema** | Flexible (can handle mixed types per column) | Strict (one type per column) |
| **Null handling** | Built-in resolution | Can cause errors |
| **Glue integration** | Native (works with Catalog) | Needs extra config |
| **Conversion** | Can convert to/from DataFrame | Can convert to/from DynamicFrame |

---

## Why DynamicFrames Exist

Real-world data is messy. Imagine a column "price" where some records have `25.99` (number) and others have `"twenty-five"` (string).

- **Spark DataFrame** → crashes or forces one type
- **DynamicFrame** → keeps both types, lets you resolve later

---

## Key DynamicFrame Methods

| Method | What it does |
|--------|-------------|
| `drop_fields()` | Remove columns |
| `rename_field()` | Rename a column |
| `resolveChoice()` | Handle mixed data types in a column |
| `apply_mapping()` | Rename and retype multiple columns |
| `filter()` | Filter rows based on condition |
| `toDF()` | Convert to Spark DataFrame |
| `fromDF()` | Convert from Spark DataFrame |

---

## Converting Between Types

```python
# DynamicFrame → DataFrame
spark_df = dynamic_frame.toDF()

# DataFrame → DynamicFrame
from awsglue.dynamicframe import DynamicFrame
dynamic_frame = DynamicFrame.fromDF(spark_df, glueContext, "name")
```

---

## Key Takeaway

> DynamicFrames are Glue's flexible data structures that handle messy, inconsistent data. Use them for reading from the Glue Catalog and resolving data type conflicts. Convert to DataFrames when you need standard Spark operations.

---

**Previous:** [Glue Ray Jobs](./08-Glue-Ray-Jobs.md)
**Next:** [Glue Job Bookmarks](./10-Glue-Job-Bookmarks.md)

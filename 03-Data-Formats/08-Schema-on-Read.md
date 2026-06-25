# Schema on Read

## What is Schema on Read?

**Schema on Read** means you define the structure of data **when you read it**, not when you store it.

The data is stored **raw** — no rules about structure are applied at storage time.

---

## How It Works

1. Store raw data in S3 (any format — CSV, JSON, Parquet)
2. When you want to query it, **define the schema at that point**
3. Different users can apply **different schemas** to the same data

---

## Example

You store a raw JSON file in S3:
```json
{"name": "Tanishq", "age": 25, "city": "Delhi"}
```

- Analyst A queries it as: `name (string), age (int), city (string)`
- Analyst B ignores "city" and queries: `name (string), age (int)`

Both are valid — the schema is applied **when reading**.

---

## Where Schema on Read is Used

| Service | How |
|---------|-----|
| **Amazon S3** | Stores data with no schema |
| **Amazon Athena** | Applies schema when querying S3 |
| **AWS Glue Crawlers** | Discover and apply schema to S3 data |
| **Data Lakes** | Schema on Read by nature |

---

## Pros and Cons

| Pros | Cons |
|------|------|
| ✅ Very flexible | ❌ No data validation at write time |
| ✅ Store now, figure out later | ❌ Bad data can sneak in |
| ✅ Different views of same data | ❌ Slower queries (must interpret at read) |

---

## Key Takeaway

> Schema on Read = define structure when you read, not when you store. Data lakes use Schema on Read. It's flexible but requires good data governance.

---

**Previous:** [Row vs Columnar Formats](./07-Row-vs-Columnar-Formats.md)
**Next:** [Schema on Write](./09-Schema-on-Write.md)

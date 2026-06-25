# S3 Buckets

## What is a Bucket?

A **bucket** is a container that holds your objects (files) in S3. Every object must live inside a bucket.

Think of a bucket like a **top-level folder** — but with some special rules.

---

## Bucket Rules

| Rule | Detail |
|------|--------|
| **Globally unique name** | No two buckets in the world can have the same name |
| **Region-specific** | Each bucket is created in a specific AWS Region |
| **Naming** | Lowercase letters, numbers, hyphens only. 3-63 characters |
| **No nesting** | You cannot create a bucket inside another bucket |
| **Limit** | 100 buckets per account by default (can request more) |

---

## Bucket Naming Examples

✅ Valid: `my-data-lake-2024`, `company-sales-raw`, `tanishq-analytics`

❌ Invalid: `My_Bucket` (uppercase + underscore), `s3://bucket` (no prefix needed)

---

## "Folders" in S3

S3 doesn't actually have folders. It uses **prefixes** that look like folders:

```
s3://my-bucket/raw/sales/2024/january/data.parquet
```

- Bucket: `my-bucket`
- Prefix (fake folder path): `raw/sales/2024/january/`
- Object: `data.parquet`

The console shows these as folders, but technically everything is a flat list of keys.

---

## Common Bucket Structure for Data Lakes

```
s3://company-data-lake/
├── raw/            ← Original, untouched data
├── processed/      ← Cleaned and transformed data
├── curated/        ← Final, ready-for-analysis data
└── archive/        ← Old data moved to cheaper storage
```

---

## Key Takeaway

> Buckets are top-level containers in S3 with globally unique names. They don't have real folders — just key prefixes that look like paths. Design your bucket structure carefully for your data lake.

---

**Previous:** [What is S3](./01-What-is-S3.md)
**Next:** [S3 Objects](./03-S3-Objects.md)

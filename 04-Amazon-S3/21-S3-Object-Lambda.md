# S3 Object Lambda

## What is S3 Object Lambda?

**S3 Object Lambda** lets you **transform data on-the-fly** when it's retrieved from S3 — without changing the original stored object.

---

## How It Works

```
App requests file from S3
    → S3 Object Lambda Access Point
    → Triggers a Lambda function
    → Lambda transforms the data
    → App receives the transformed data
    → Original file in S3 stays unchanged
```

---

## Use Cases

| Use Case | What Lambda Does |
|----------|-----------------|
| **Redact PII** | Remove names, SSNs before returning data |
| **Format conversion** | Convert XML to JSON on read |
| **Resize images** | Return smaller image for mobile apps |
| **Filter rows** | Return only rows relevant to the user |
| **Enrich data** | Add extra info from another database |

---

## Key Points

- Original object is **never modified**
- Different users can see **different versions** of the same object
- Requires an **S3 Object Lambda Access Point**
- Uses AWS Lambda (pay per invocation)

---

## Key Takeaway

> S3 Object Lambda transforms data as it's read without modifying the original. Great for PII redaction, format conversion, and per-user data customization.

---

**Previous:** [S3 Select](./20-S3-Select.md)
**Next:** [S3 Replication](./22-S3-Replication.md)

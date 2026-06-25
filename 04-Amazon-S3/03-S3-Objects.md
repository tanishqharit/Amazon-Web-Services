# S3 Objects

## What is an Object?

An **object** is a file stored in S3. It can be anything — a CSV, a Parquet file, an image, a video, a log file.

Every object has three parts:

| Part | Description | Example |
|------|-------------|---------|
| **Key** | The full path/name of the object | `raw/sales/2024/data.parquet` |
| **Value** | The actual data (file content) | The bytes of the file |
| **Metadata** | Extra info about the object | Content type, upload date, custom tags |

---

## Object Key

The **key** is the unique identifier for an object within a bucket.

```
s3://my-bucket/raw/sales/2024/january/data.parquet
               └──────────── Key ────────────────┘
```

---

## Object Size Limits

| Limit | Value |
|-------|-------|
| Minimum size | 0 bytes (empty file) |
| Maximum size | **5 TB** |
| Single PUT upload limit | 5 GB |
| For files > 5 GB | Must use **Multipart Upload** |

---

## Object Metadata

Each object has metadata — info about the object:

**System metadata** (set by AWS):
- Content-Type (e.g., `application/json`)
- Last-Modified date
- Content-Length (file size)

**User metadata** (set by you):
- Custom key-value pairs (e.g., `department: sales`)
- Must start with `x-amz-meta-`

---

## Object Tags

Tags are key-value pairs you attach to objects for:
- **Cost tracking** (tag by department)
- **Lifecycle rules** (delete objects with tag `temp: true` after 30 days)
- **Access control** (allow access only to objects tagged `confidential: false`)

---

## Key Takeaway

> Objects are files stored in S3. Each object has a Key (path), Value (data), and Metadata. Max size is 5 TB. Use tags for organization, cost tracking, and access control.

---

**Previous:** [S3 Buckets](./02-S3-Buckets.md)
**Next:** [S3 Storage Classes Overview](./04-S3-Storage-Classes-Overview.md)

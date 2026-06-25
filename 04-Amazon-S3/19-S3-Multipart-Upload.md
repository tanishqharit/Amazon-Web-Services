# S3 Multipart Upload

## What is Multipart Upload?

**Multipart Upload** breaks a large file into smaller parts and uploads them **in parallel**. This makes uploading big files much faster and more reliable.

---

## How It Works

```
100 GB file
├── Part 1 (10 GB) → Upload in parallel ─┐
├── Part 2 (10 GB) → Upload in parallel ─┤
├── Part 3 (10 GB) → Upload in parallel ─┤
├── ...                                   ├→ S3 reassembles → Complete file
└── Part 10 (10 GB) → Upload in parallel ─┘
```

---

## Key Rules

| Rule | Detail |
|------|--------|
| **Required for** | Files > 5 GB (mandatory) |
| **Recommended for** | Files > 100 MB |
| **Max parts** | 10,000 |
| **Part size** | 5 MB to 5 GB each |
| **Retry** | If one part fails, only retry that part |

---

## Benefits

- ✅ **Faster** — parallel uploads
- ✅ **Resilient** — retry individual parts on failure
- ✅ **Required** for files over 5 GB
- ✅ **Pause and resume** — can continue interrupted uploads

---

## Cleaning Up

If a multipart upload is **never completed**, the parts stay in S3 and cost money. Use a **lifecycle policy** to automatically delete incomplete multipart uploads:

```
Delete incomplete multipart uploads after 7 days
```

---

## Key Takeaway

> Multipart Upload splits large files into parts and uploads them in parallel. Required for files > 5 GB, recommended for > 100 MB. Always set a lifecycle policy to clean up incomplete uploads.

---

**Previous:** [S3 Transfer Acceleration](./18-S3-Transfer-Acceleration.md)
**Next:** [S3 Select](./20-S3-Select.md)

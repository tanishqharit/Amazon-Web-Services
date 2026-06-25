# Data Compression

## What is Data Compression?

**Data compression** reduces the size of data files so they take up **less storage space** and are **faster to transfer**.

Think of it like vacuum-packing clothes — same clothes, much smaller suitcase.

---

## Why Compression Matters on AWS

1. **Lower storage cost** — smaller files = less S3 cost
2. **Faster queries** — less data to scan = faster Athena/Redshift queries
3. **Lower data transfer cost** — less data moving between services
4. **Athena billing** — you pay per TB scanned (compressed data = cheaper)

---

## Common Compression Formats

| Format | Speed | Compression Ratio | Splittable? | Best For |
|--------|-------|-------------------|-------------|----------|
| **Snappy** | ⚡ Very fast | Medium | Yes (with Parquet) | General use, Spark jobs |
| **GZIP** | Slow | High | ❌ No | Maximum compression |
| **Zstd** | Fast | High | Yes (with Parquet) | Best balance of speed + size |
| **LZO** | Fast | Medium | Yes | Hadoop/EMR |
| **BZIP2** | Very slow | Very high | Yes | Archival |

---

## What Does "Splittable" Mean?

A **splittable** file can be broken into pieces and processed in parallel by multiple workers.

- **Splittable** = faster processing (Spark/EMR can parallelize)
- **Not splittable** = one worker must process the whole file

GZIP is NOT splittable — but **Parquet + GZIP** is splittable because Parquet handles the splitting.

---

## Recommended Combinations

| Combination | Use Case |
|-------------|----------|
| **Parquet + Snappy** | Default for most data lakes ⭐ |
| **Parquet + Zstd** | When you want smaller files |
| **Parquet + GZIP** | When storage cost is the top priority |

---

## Key Takeaway

> Compression reduces file size, storage cost, and query time. For AWS data lakes, use Parquet + Snappy as the default. Snappy is fast, Zstd is balanced, GZIP is smallest.

---

**Previous:** [Schema on Write](./09-Schema-on-Write.md)
**Next:** [Choosing the Right Format](./11-Choosing-the-Right-Format.md)

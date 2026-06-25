# Firehose Buffering

## What is Buffering?

Firehose doesn't deliver data instantly. It **collects records in a buffer** and delivers them in batches. This is why Firehose is **near-real-time**, not real-time.

---

## Buffer Settings

| Setting | Range | Default |
|---------|-------|---------|
| **Buffer size** | 1 MB — 128 MB | 5 MB |
| **Buffer interval** | 60 sec — 900 sec | 300 sec (5 min) |

Firehose delivers data when **either** condition is met first.

---

## How It Works

```
Example: Buffer size = 5 MB, Buffer interval = 60 seconds

Scenario A: 5 MB of data arrives in 30 seconds
→ Delivers immediately (buffer size reached first)

Scenario B: Only 1 MB of data in 60 seconds
→ Delivers after 60 seconds (buffer time reached first)
```

---

## Tuning the Buffer

| Want | Adjust |
|------|--------|
| **Faster delivery** | ↓ Decrease buffer size and interval |
| **Fewer, larger files** | ↑ Increase buffer size and interval |
| **Fastest possible** | Buffer size = 1 MB, interval = 60 sec |

---

## Small File Problem

If your buffer is too small, Firehose creates **many small files** in S3. This hurts query performance (Athena, Spark).

**Solution:** Use larger buffer settings, or run a periodic **Glue compaction job** to merge small files.

---

## Key Takeaway

> Firehose buffers data before delivery (min 60 seconds). Tune buffer size and interval based on your needs. Watch out for the small file problem — too many small files hurt analytics performance.

---

**Previous:** [Firehose Data Transformation](./09-Firehose-Data-Transformation.md)
**Next:** [Kinesis Data Streams vs Firehose](./11-Kinesis-Data-Streams-vs-Firehose.md)

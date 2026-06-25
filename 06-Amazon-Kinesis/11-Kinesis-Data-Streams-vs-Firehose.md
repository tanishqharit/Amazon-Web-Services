# Kinesis Data Streams vs Firehose

## The Most Important Comparison

This comes up **constantly** on the exam.

---

## Side-by-Side

| Feature | Kinesis Data Streams | Kinesis Firehose |
|---------|---------------------|------------------|
| **Purpose** | Ingest & process real-time data | Deliver data to destinations |
| **Latency** | Real-time (~200 ms) | Near-real-time (60+ sec buffer) |
| **Scaling** | Manual (shards) or On-Demand | Automatic |
| **Data retention** | 24 hours — 365 days | No retention (delivers and done) |
| **Consumers** | Custom (Lambda, KCL, SDK) | Built-in (S3, Redshift, OpenSearch) |
| **Transforms** | You build it | Lambda integration built-in |
| **Management** | You manage shards | Fully managed |
| **Replay** | ✅ Yes (read data again) | ❌ No |
| **Pricing** | Per shard hour | Per data volume |

---

## When to Use Data Streams

- ✅ Need **real-time** processing (< 1 second)
- ✅ Need to **replay** data
- ✅ Need **multiple consumers** reading the same data
- ✅ Need **custom processing** logic
- ✅ Need to **retain data** for days

---

## When to Use Firehose

- ✅ Just need to **deliver data to S3/Redshift/OpenSearch**
- ✅ Want **zero management** (no shards)
- ✅ Need **automatic format conversion** (JSON → Parquet)
- ✅ **Near-real-time** is acceptable
- ✅ Don't need to replay data

---

## Common Pattern: Use Both Together

```
Producers → Kinesis Data Streams → Kinesis Firehose → S3 (Parquet)
                                 → Lambda (real-time alerts)
```

Data Streams for ingestion, Firehose for delivery to storage.

---

## Exam Keyword Triggers

| Keyword | Choose |
|---------|--------|
| "Real-time" | Data Streams |
| "Near-real-time delivery to S3" | Firehose |
| "Replay data" | Data Streams |
| "No server management" | Firehose |
| "Convert to Parquet" | Firehose |
| "Multiple consumers" | Data Streams |

---

## Key Takeaway

> Data Streams = real-time ingestion with custom processing. Firehose = near-real-time delivery to S3/Redshift with zero management. Often used together. This comparison is heavily tested.

---

**Previous:** [Firehose Buffering](./10-Firehose-Buffering.md)
**Next:** [Kinesis Data Analytics](./12-Kinesis-Data-Analytics.md)

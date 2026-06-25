# Firehose Delivery Streams

## What is a Delivery Stream?

A **delivery stream** is the main resource in Firehose. You create a delivery stream, configure its source, transformations, and destination.

---

## Sources for Firehose

| Source | How data gets in |
|--------|-----------------|
| **Direct PUT** | Applications send data directly via API |
| **Kinesis Data Streams** | Firehose reads from a KDS stream |
| **Amazon MSK** | Firehose reads from Kafka topics |
| **CloudWatch Logs** | Subscriptions send logs |
| **AWS IoT** | IoT rules send device data |

---

## Configuration Options

| Setting | Options |
|---------|---------|
| **Source** | Direct PUT or KDS/MSK |
| **Transform** | Lambda function (optional) |
| **Format conversion** | JSON → Parquet/ORC (optional) |
| **Compression** | GZIP, Snappy, Zip, Hadoop Snappy |
| **Encryption** | SSE-KMS |
| **Buffer** | Size (1-128 MB) and time (60-900 sec) |
| **Backup** | Save original data to backup S3 bucket |

---

## Backup Configuration

Firehose can save a **backup copy** of the original (untransformed) data to a separate S3 bucket. This is useful when:
- Transformation fails → you still have the raw data
- You need to reprocess from original format

---

## Key Takeaway

> A delivery stream is Firehose's core resource. It takes data from sources (Direct PUT, KDS, MSK), optionally transforms it, and delivers to destinations. Always consider enabling backup for raw data.

---

**Previous:** [Kinesis Data Firehose Overview](./07-Kinesis-Data-Firehose-Overview.md)
**Next:** [Firehose Data Transformation](./09-Firehose-Data-Transformation.md)

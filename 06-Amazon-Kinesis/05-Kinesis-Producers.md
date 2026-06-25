# Kinesis Producers

## What is a Producer?

A **producer** is anything that **sends data** into a Kinesis Data Stream.

---

## Types of Producers

| Producer | What it is | Best for |
|----------|-----------|----------|
| **AWS SDK** | Code using Boto3 or Java SDK | Simple, low-volume |
| **Kinesis Producer Library (KPL)** | High-performance library | High-volume, batching |
| **Kinesis Agent** | Pre-built agent for log files | Monitoring log files on servers |
| **AWS services** | CloudWatch, IoT | Automatic integration |

---

## AWS SDK (Simple Producer)

```python
import boto3

kinesis = boto3.client('kinesis')
kinesis.put_record(
    StreamName='my-stream',
    Data=b'{"user": "tanishq", "action": "click"}',
    PartitionKey='user_tanishq'
)
```

Simple, but limited to **1 record at a time** per call (or `put_records` for batch).

---

## Kinesis Producer Library (KPL)

- Batches multiple records into one API call
- Compresses data automatically
- Handles retries and errors
- **Higher throughput** than raw SDK
- Adds small latency (buffering for batching)

---

## Kinesis Agent

- Install on EC2 instances
- Monitors log files and sends them to Kinesis
- No code needed — just configuration
- Handles file rotation automatically

---

## Key Takeaway

> Producers send data to Kinesis. Use SDK for simple use cases, KPL for high-volume production, and Kinesis Agent for log files. KPL batches and compresses for better performance.

---

**Previous:** [Kinesis Partition Keys](./04-Kinesis-Partition-Keys.md)
**Next:** [Kinesis Consumers](./06-Kinesis-Consumers.md)

# Kinesis Consumers

## What is a Consumer?

A **consumer** is anything that **reads data** from a Kinesis Data Stream and processes it.

---

## Types of Consumers

| Consumer | What it is | Best for |
|----------|-----------|----------|
| **AWS Lambda** | Serverless function triggered by stream | Simple processing |
| **Kinesis Client Library (KCL)** | Custom consumer app | Complex processing, multiple consumers |
| **AWS SDK** | Read with code | Simple, low-volume |
| **Kinesis Data Firehose** | Deliver to S3/Redshift | Loading to storage |
| **Kinesis Data Analytics** | SQL/Flink on stream | Real-time analytics |

---

## Shared vs Enhanced Fan-Out

| Mode | Read Speed | How it works |
|------|-----------|-------------|
| **Shared (default)** | 2 MB/sec per shard (shared among all consumers) | Consumers poll for data |
| **Enhanced Fan-Out** | 2 MB/sec per shard **per consumer** | Data pushed to consumers |

Example with 3 consumers and 1 shard:
- **Shared:** 3 consumers share 2 MB/sec = ~0.67 MB/sec each
- **Enhanced Fan-Out:** Each consumer gets its own 2 MB/sec

---

## When to Use Enhanced Fan-Out

- Multiple consumers reading the same stream
- Low-latency requirements (sub-200ms)
- Higher cost but much better performance

---

## Lambda as a Consumer

- AWS Lambda can be triggered by Kinesis
- Lambda reads batches of records
- Great for simple event processing
- Limited by Lambda timeout (15 min max)

---

## Key Takeaway

> Consumers read and process stream data. Use Lambda for simple processing, KCL for complex apps. Use Enhanced Fan-Out when multiple consumers need full throughput from the same stream.

---

**Previous:** [Kinesis Producers](./05-Kinesis-Producers.md)
**Next:** [Kinesis Data Firehose Overview](./07-Kinesis-Data-Firehose-Overview.md)

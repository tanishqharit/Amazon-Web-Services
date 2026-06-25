# Stream Processing

## What is Stream Processing?

**Stream processing** means processing data **immediately as it arrives**, one record at a time or in small batches.

Think of it like a car wash:
- Each car is washed the moment it arrives
- You don't wait for 100 cars to show up
- That's stream processing!

---

## How It Works

```
Data arrives → Process immediately → Output in real-time
  (continuous)    (instant)           (seconds/milliseconds)
```

---

## Characteristics

| Feature | Stream Processing |
|---------|------------------|
| **When** | Continuously (as data arrives) |
| **Data volume** | Small pieces at a time |
| **Latency** | Low (seconds or less) |
| **Complexity** | More complex to build |
| **Cost** | Can be higher (always running) |

---

## Real Examples

1. **Fraud detection** — flag suspicious credit card transactions instantly
2. **Live dashboards** — show website visitors in real-time
3. **IoT sensors** — monitor factory temperature every second
4. **Social media feeds** — process and display new posts as they happen

---

## AWS Services for Stream Processing

| Service | How it's used |
|---------|--------------|
| **Amazon Kinesis Data Streams** | Real-time data ingestion |
| **Amazon Kinesis Data Firehose** | Near-real-time delivery to S3/Redshift |
| **Amazon MSK** | Managed Apache Kafka for streaming |
| **AWS Lambda** | Process individual stream records |
| **Apache Flink (Managed)** | Complex stream analytics |

---

## Key Takeaway

> Stream processing handles data the moment it arrives. It gives you real-time results but is more complex and can cost more. Use it when you need instant insights.

---

**Previous:** [Batch Processing](./08-Batch-Processing.md)
**Next:** [Batch vs Streaming](./10-Batch-vs-Streaming.md)

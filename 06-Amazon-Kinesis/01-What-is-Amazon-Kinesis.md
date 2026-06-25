# What is Amazon Kinesis?

## Simple Explanation

**Amazon Kinesis** is a family of services for **real-time streaming data**. It lets you collect, process, and analyze data as it arrives — in real-time.

Think of Kinesis like a **conveyor belt** in a factory — data flows continuously and you can process it as it passes by.

---

## The Kinesis Family

| Service | Purpose |
|---------|---------|
| **Kinesis Data Streams** | Collect and process real-time data |
| **Kinesis Data Firehose** | Deliver streaming data to destinations |
| **Kinesis Data Analytics** | Analyze streaming data with SQL/Flink |

---

## When to Use Kinesis

- Real-time log processing
- Live dashboards and monitoring
- Fraud detection
- IoT sensor data collection
- Clickstream analytics
- Social media feed processing

---

## Kinesis in a Data Pipeline

```
Data Producers    →    Kinesis    →    Consumers/Destinations
(apps, IoT,           (streaming       (S3, Redshift, Lambda,
 servers, logs)        service)          real-time analytics)
```

---

## Key Takeaway

> Kinesis is AWS's real-time streaming platform. It has Data Streams (ingest), Firehose (deliver), and Data Analytics (analyze). Use it whenever the exam says "real-time" or "streaming."

---

**Next:** [Kinesis Data Streams Overview](./02-Kinesis-Data-Streams-Overview.md)

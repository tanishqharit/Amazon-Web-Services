# Kinesis Data Streams Overview

## What is Kinesis Data Streams (KDS)?

**Kinesis Data Streams** is a service for **ingesting real-time data** at massive scale. You can push data in from thousands of sources and process it with consumers in real-time.

---

## Key Concepts

| Concept | Description |
|---------|-------------|
| **Stream** | A named group of shards that hold your data |
| **Shard** | A unit of capacity in a stream |
| **Record** | A single piece of data (up to 1 MB) |
| **Partition Key** | Determines which shard a record goes to |
| **Sequence Number** | Unique ID assigned to each record |
| **Retention** | How long data stays (default 24 hours, max 365 days) |

---

## How It Works

```
Producers → Put records into Stream → Shards hold data → Consumers read data
```

Example:
```
Mobile apps (producers)
    → Write click events to a Kinesis Stream
    → Data goes to shards based on partition key
    → Lambda functions (consumers) process each event
```

---

## Key Features

| Feature | Detail |
|---------|--------|
| **Real-time** | Sub-second latency |
| **Scalable** | Add more shards for more throughput |
| **Durable** | Data replicated across 3 AZs |
| **Retention** | 24 hours default, up to 365 days |
| **Ordering** | Records are ordered within a shard |

---

## Key Takeaway

> Kinesis Data Streams ingests real-time data at scale. Data flows through shards and is read by consumers. Records are ordered within each shard. Default retention is 24 hours.

---

**Previous:** [What is Amazon Kinesis](./01-What-is-Amazon-Kinesis.md)
**Next:** [Kinesis Shards](./03-Kinesis-Shards.md)

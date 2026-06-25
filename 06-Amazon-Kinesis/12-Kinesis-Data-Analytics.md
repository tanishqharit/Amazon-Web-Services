# Kinesis Data Analytics (Apache Flink)

## What is it?

**Kinesis Data Analytics** lets you analyze streaming data in real-time using **Apache Flink** or **SQL**.

> **Note:** AWS renamed this to **Amazon Managed Service for Apache Flink**, but the exam may use either name.

---

## Two Options

| Option | Language | Best For |
|--------|----------|----------|
| **Apache Flink** | Java, Scala, Python | Complex stream processing |
| **SQL** (legacy) | SQL | Simple analytics (being deprecated) |

---

## What Apache Flink Can Do

- **Windowed aggregations** — calculate metrics over time windows (e.g., average per 5 minutes)
- **Pattern detection** — find specific event sequences
- **Real-time dashboards** — continuous metrics calculation
- **Anomaly detection** — spot unusual patterns instantly

---

## Sources and Destinations

| Sources | Destinations |
|---------|-------------|
| Kinesis Data Streams | Kinesis Data Streams |
| Amazon MSK (Kafka) | Kinesis Firehose |
| | Amazon S3 |
| | Custom (via Flink connectors) |

---

## Example Use Case

```
Clickstream data → Kinesis Data Streams → Flink Application → Real-time dashboard
                                                            → Alert if > 1000 errors/min
```

---

## Key Takeaway

> Kinesis Data Analytics (Apache Flink) processes streaming data in real-time with complex logic. Use it for windowed aggregations, pattern detection, and real-time analytics. More powerful than simple Lambda consumers.

---

**Previous:** [Kinesis Data Streams vs Firehose](./11-Kinesis-Data-Streams-vs-Firehose.md)
**Next:** [Kinesis Scaling](./13-Kinesis-Scaling.md)

# Batch vs Streaming

## Side-by-Side Comparison

| Feature | Batch | Streaming |
|---------|-------|-----------|
| **Processing** | All at once (scheduled) | As data arrives (continuous) |
| **Latency** | Minutes to hours | Seconds to milliseconds |
| **Data size** | Large volumes | Small, continuous pieces |
| **Complexity** | Simpler | More complex |
| **Cost** | Usually cheaper | Can be more expensive |
| **Use case** | Reports, analytics | Alerts, live dashboards |

---

## When to Use Batch

- ✅ Data doesn't need to be real-time
- ✅ Processing large historical datasets
- ✅ Nightly data warehouse loads
- ✅ Monthly reports and billing
- ✅ Cost is a priority

---

## When to Use Streaming

- ✅ Data must be processed immediately
- ✅ Fraud detection, security alerts
- ✅ Live dashboards and monitoring
- ✅ IoT sensor data
- ✅ Real-time recommendations

---

## Can You Use Both?

**Yes!** Many real-world systems use both. This is called the **Lambda Architecture**:

```
Data Source
├── Batch Layer: Process all data daily (Glue → S3 → Redshift)
└── Speed Layer: Process real-time data (Kinesis → Lambda → DynamoDB)
```

---

## For the Exam — Keyword Triggers

| Exam Keyword | Choose |
|-------------|--------|
| "Real-time" | Streaming (Kinesis Data Streams) |
| "Near-real-time" | Streaming (Kinesis Firehose) |
| "Daily", "Nightly", "Scheduled" | Batch (Glue, EMR) |
| "Historical analysis" | Batch |
| "Immediate alerts" | Streaming |
| "Cost-effective" | Usually batch |

---

## Key Takeaway

> Batch is for scheduled, large-volume processing. Streaming is for real-time, continuous processing. Many systems use both. The exam will test you on knowing which to choose based on the scenario.

---

**Previous:** [Stream Processing](./09-Stream-Processing.md)
**Next:** [Structured Data](./11-Structured-Data.md)

# Kinesis Best Practices

## Performance

1. **Use high-cardinality partition keys** — avoid hot shards
2. **Use KPL for high-volume producers** — batching + compression
3. **Use Enhanced Fan-Out** for multiple consumers
4. **Right-size your shards** — monitor with CloudWatch metrics
5. **Use On-Demand mode** when traffic is unpredictable

## Cost

1. **Use Firehose** when you just need to deliver to S3 — cheaper than KDS + custom consumer
2. **Reduce retention** to minimum needed (default 24 hours)
3. **Merge idle shards** to save money
4. **Use Firehose format conversion** instead of running a separate Glue job

## Architecture

1. **KDS + Firehose pattern:** Use KDS for ingestion, Firehose for delivery to S3
2. **Lambda for simple processing:** Don't over-engineer — Lambda handles most use cases
3. **Flink for complex analytics:** Use when you need windowed aggregations or pattern matching

---

## Exam Tips for Kinesis

| Question Pattern | Answer |
|-----------------|--------|
| "Real-time ingestion" | Kinesis Data Streams |
| "Deliver to S3 with no management" | Firehose |
| "Convert streaming JSON to Parquet" | Firehose format conversion |
| "Multiple consumers, full throughput" | Enhanced Fan-Out |
| "Process only new data, ordered" | Use partition keys in KDS |
| "ProvisionedThroughputExceededException" | More shards or On-Demand |
| "Complex real-time analytics" | Kinesis Data Analytics (Flink) |
| "Near-real-time vs real-time" | Firehose vs Data Streams |

---

## Key Takeaway

> Know when to use Data Streams vs Firehose vs Flink. Use high-cardinality partition keys. Choose On-Demand for unpredictable traffic. Firehose + format conversion is the easiest streaming-to-Parquet path.

---

**Previous:** [Kinesis Scaling](./13-Kinesis-Scaling.md)
**Next:** [Section 07 — Amazon Redshift](../07-Amazon-Redshift/01-What-is-Amazon-Redshift.md)

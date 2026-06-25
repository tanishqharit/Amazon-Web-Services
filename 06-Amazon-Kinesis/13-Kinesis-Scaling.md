# Kinesis Scaling

## Scaling Kinesis Data Streams

### Provisioned Mode
You manually set the number of **shards**.

- **Scale up:** Split shards (1 shard → 2 shards)
- **Scale down:** Merge shards (2 shards → 1 shard)
- Limitation: Can only split/merge **one shard at a time**
- Takes time — not instant

### On-Demand Mode
AWS manages scaling automatically.

- No shard management needed
- Scales up to 200 MB/sec write, 400 MB/sec read by default
- More expensive per GB but zero management
- Best for unpredictable traffic

---

## Scaling Kinesis Firehose

Firehose scales **automatically**. No manual intervention needed.

---

## Common Scaling Issues

| Problem | Cause | Solution |
|---------|-------|----------|
| `ProvisionedThroughputExceededException` | Shard capacity exceeded | Add more shards or use On-Demand |
| Hot shard | Bad partition key | Use high-cardinality partition keys |
| Slow consumers | Consumer can't keep up | Use Enhanced Fan-Out |

---

## Key Takeaway

> KDS scales via shard management (Provisioned) or automatically (On-Demand). Firehose always auto-scales. Watch for throughput exceeded errors — they mean you need more shards or better partition keys.

---

**Previous:** [Kinesis Data Analytics](./12-Kinesis-Data-Analytics.md)
**Next:** [Kinesis Best Practices](./14-Kinesis-Best-Practices.md)

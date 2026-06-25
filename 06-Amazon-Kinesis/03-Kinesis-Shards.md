# Kinesis Shards

## What is a Shard?

A **shard** is a unit of capacity in a Kinesis Data Stream. Think of each shard as a **lane on a highway** — more lanes = more traffic capacity.

---

## Shard Capacity

| Direction | Capacity per Shard |
|-----------|-------------------|
| **Write (ingest)** | 1 MB/sec OR 1,000 records/sec |
| **Read (consume)** | 2 MB/sec |

---

## Scaling with Shards

| Shards | Write Capacity | Read Capacity |
|--------|---------------|---------------|
| 1 | 1 MB/sec | 2 MB/sec |
| 2 | 2 MB/sec | 4 MB/sec |
| 10 | 10 MB/sec | 20 MB/sec |
| 100 | 100 MB/sec | 200 MB/sec |

More shards = more cost, but more throughput.

---

## Provisioned vs On-Demand Mode

| Mode | How it works |
|------|-------------|
| **Provisioned** | You specify the number of shards. You pay per shard. |
| **On-Demand** | AWS auto-scales shards. You pay per data throughput. |

- **Provisioned** → when you know your throughput needs
- **On-Demand** → when traffic is unpredictable

---

## Shard Splitting and Merging

- **Splitting** — divide one shard into two (increase capacity)
- **Merging** — combine two shards into one (decrease capacity/cost)
- Cannot split/merge more than one shard at a time

---

## Key Takeaway

> Shards are the scaling unit of Kinesis. Each shard handles 1 MB/sec write and 2 MB/sec read. More shards = more throughput but higher cost. Use On-Demand mode when traffic is unpredictable.

---

**Previous:** [Kinesis Data Streams Overview](./02-Kinesis-Data-Streams-Overview.md)
**Next:** [Kinesis Partition Keys](./04-Kinesis-Partition-Keys.md)

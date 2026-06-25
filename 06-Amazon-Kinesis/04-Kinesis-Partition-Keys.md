# Kinesis Partition Keys

## What is a Partition Key?

A **partition key** is a string that you assign to each record. Kinesis uses it to determine **which shard** the record goes to.

---

## How It Works

```
Record with partition key → Hash function → Shard assignment

"user_123" → hash → Shard 1
"user_456" → hash → Shard 2
"user_123" → hash → Shard 1  (same key = same shard!)
```

Records with the **same partition key** always go to the **same shard**.

---

## Why It Matters

### Ordering
Records in the same shard are **ordered**. So if you want all events for a specific user to be in order, use the **user ID** as the partition key.

### Hot Shards ⚠️
If too many records use the same partition key, one shard gets overloaded while others are idle. This is called a **"hot shard"**.

```
Bad:  All records → partition key "default" → ALL go to Shard 1 (overloaded!)
Good: Records → partition key = user_id → evenly spread across shards
```

---

## Best Practices

| Practice | Why |
|----------|-----|
| Use a **high-cardinality** key | Spreads data evenly (e.g., user ID, device ID) |
| Avoid **low-cardinality** keys | Causes hot shards (e.g., country name with few values) |
| Use **random keys** if order doesn't matter | Best distribution |

---

## Key Takeaway

> Partition keys determine which shard a record goes to. Same key = same shard = ordered records. Use high-cardinality keys to avoid hot shards.

---

**Previous:** [Kinesis Shards](./03-Kinesis-Shards.md)
**Next:** [Kinesis Producers](./05-Kinesis-Producers.md)

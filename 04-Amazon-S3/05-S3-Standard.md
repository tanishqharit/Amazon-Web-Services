# S3 Standard

## What is S3 Standard?

**S3 Standard** is the default storage class. It's designed for **frequently accessed data** that needs instant availability.

---

## Key Features

| Feature | Detail |
|---------|--------|
| **Access** | Instant (milliseconds) |
| **Durability** | 99.999999999% (11 nines) |
| **Availability** | 99.99% |
| **AZs** | Stored across ≥ 3 AZs |
| **Retrieval fee** | None |
| **Min storage duration** | None |
| **Cost** | Highest storage cost, no retrieval cost |

---

## When to Use

- Data accessed **multiple times per day**
- Active data lake data being queried
- Hot data in pipelines
- Websites, apps, frequently read files

---

## Key Takeaway

> S3 Standard is the default for frequently accessed data. Highest storage cost but no retrieval fees. Data is replicated across 3+ AZs for maximum durability.

---

**Previous:** [S3 Storage Classes Overview](./04-S3-Storage-Classes-Overview.md)
**Next:** [S3 Intelligent-Tiering](./06-S3-Intelligent-Tiering.md)

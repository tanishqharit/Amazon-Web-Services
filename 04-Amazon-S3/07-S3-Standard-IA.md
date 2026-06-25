# S3 Standard-IA (Infrequent Access)

## What is S3 Standard-IA?

**S3 Standard-IA** is for data that is accessed **less often** but needs **instant access** when requested.

IA = Infrequent Access.

---

## Key Features

| Feature | Detail |
|---------|--------|
| **Access** | Instant (milliseconds) |
| **Storage cost** | ~40% cheaper than S3 Standard |
| **Retrieval fee** | Yes (per GB retrieved) |
| **Min storage duration** | 30 days (charged even if deleted earlier) |
| **Min object size** | 128 KB (charged even if smaller) |
| **AZs** | Stored across ≥ 3 AZs |

---

## When to Use

- Data accessed **once a month or less**
- Backups that might be needed occasionally
- Older data lake partitions rarely queried
- Disaster recovery copies

---

## When NOT to Use

- ❌ Data accessed daily → use S3 Standard
- ❌ Very small files (< 128 KB) → charged for 128 KB anyway
- ❌ Files deleted within 30 days → still charged for 30 days

---

## Key Takeaway

> Standard-IA is cheaper for storage but charges for retrieval. Use it for data you access rarely but need instantly. Remember the 30-day minimum and 128 KB minimum charge.

---

**Previous:** [S3 Intelligent-Tiering](./06-S3-Intelligent-Tiering.md)
**Next:** [S3 One Zone-IA](./08-S3-One-Zone-IA.md)

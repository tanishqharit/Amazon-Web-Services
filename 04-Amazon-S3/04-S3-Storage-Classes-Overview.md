# S3 Storage Classes Overview

## What are Storage Classes?

S3 offers different **storage classes** — each designed for a different use case. They differ in **cost, access speed, and availability**.

Think of it like hotel rooms:
- Luxury suite = expensive but instant service (S3 Standard)
- Budget room = cheap but slower service (Glacier)

---

## All Storage Classes at a Glance

| Storage Class | Access Speed | Cost | Best For |
|--------------|-------------|------|----------|
| **S3 Standard** | Instant | $$$ | Frequently accessed data |
| **S3 Intelligent-Tiering** | Instant | $$-$$$ | Unknown access patterns |
| **S3 Standard-IA** | Instant | $$ | Infrequent but quick access |
| **S3 One Zone-IA** | Instant | $ | Infrequent, non-critical data |
| **S3 Glacier Instant Retrieval** | Instant | $ | Archive with instant access |
| **S3 Glacier Flexible Retrieval** | Minutes-hours | ¢¢ | Archive, can wait |
| **S3 Glacier Deep Archive** | 12-48 hours | ¢ | Long-term archive, rarely accessed |

---

## How to Choose

```
How often do you access the data?

├── Frequently (daily) → S3 Standard
├── Don't know → S3 Intelligent-Tiering
├── Rarely (monthly) → S3 Standard-IA
├── Rarely + non-critical → S3 One Zone-IA
├── Archive + need instant access → Glacier Instant Retrieval
├── Archive + can wait minutes → Glacier Flexible Retrieval
└── Archive + can wait hours/days → Glacier Deep Archive
```

---

## For the Exam

The exam loves asking about storage classes:
- "Most cost-effective for rarely accessed data" → **Standard-IA or Glacier**
- "Archive data for compliance (7 years)" → **Glacier Deep Archive**
- "Don't know access pattern" → **Intelligent-Tiering**
- "Can lose data if AZ fails" → **One Zone-IA**

Each class is covered in detail in the next notes.

---

## Key Takeaway

> S3 has 7 storage classes from hot (Standard) to cold (Deep Archive). Choose based on how often you access data and how fast you need it. This directly impacts cost.

---

**Previous:** [S3 Objects](./03-S3-Objects.md)
**Next:** [S3 Standard](./05-S3-Standard.md)

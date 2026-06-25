# S3 Intelligent-Tiering

## What is S3 Intelligent-Tiering?

**S3 Intelligent-Tiering** automatically moves objects between access tiers based on how often you access them. No performance impact, no retrieval fees.

It's the **"set it and forget it"** storage class.

---

## How It Works

S3 monitors your access patterns and moves objects automatically:

```
Object uploaded → Frequent Access tier (same as Standard)
       ↓ (30 days no access)
Infrequent Access tier (cheaper)
       ↓ (90 days no access)
Archive Instant Access tier (even cheaper)
       ↓ (optional: 90-730 days)
Deep Archive tier (cheapest)
```

If you access the object again → it moves back to Frequent Access automatically.

---

## Key Features

| Feature | Detail |
|---------|--------|
| **Access** | Instant (all tiers) |
| **Retrieval fee** | None |
| **Monitoring fee** | Small fee per object per month |
| **Min object size** | 128 KB (smaller objects stay in Frequent) |
| **Best for** | Data with unknown or changing access patterns |

---

## When to Use

- You **don't know** how often data will be accessed
- Access patterns **change over time**
- You want to **save money without managing lifecycle rules manually**

---

## Key Takeaway

> Intelligent-Tiering automatically moves data between cheap and expensive tiers based on usage. No retrieval fees. Best when you don't know the access pattern. Small monitoring fee per object.

---

**Previous:** [S3 Standard](./05-S3-Standard.md)
**Next:** [S3 Standard-IA](./07-S3-Standard-IA.md)

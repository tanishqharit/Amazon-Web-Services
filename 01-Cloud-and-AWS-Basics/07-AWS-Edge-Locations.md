# AWS Edge Locations

## What is an Edge Location?

An **Edge Location** is a small data center that AWS uses to deliver content **closer to users**.

They are used by **Amazon CloudFront** (AWS's content delivery network, or CDN).

---

## How Edge Locations Work

```
Without Edge Locations:
User in India → Request goes to US server → Slow response

With Edge Locations:
User in India → Request goes to nearby Edge Location → Fast response
```

The first time content is requested, it's fetched from the origin (your server).
After that, it's **cached** at the Edge Location so future requests are faster.

---

## Edge Locations vs Regions vs AZs

| Concept | What it is | How many? |
|---------|-----------|-----------|
| **Region** | Group of data centers in a geographic area | 30+ |
| **AZ** | Individual data center within a Region | 2-6 per Region |
| **Edge Location** | Mini cache point for fast content delivery | 400+ worldwide |

Edge Locations are **much more common** than Regions — there are 400+ around the world.

---

## Why This Matters for Data Engineering

Edge Locations are **less relevant** for core data engineering tasks. But they show up in the exam when discussing:

- Delivering dashboards and reports to global users (QuickSight)
- Transferring data faster using **S3 Transfer Acceleration** (uses Edge Locations)

---

## Key Takeaway

> Edge Locations are mini data centers for caching content closer to users. There are 400+ worldwide. They are used by CloudFront and S3 Transfer Acceleration.

---

**Previous:** [Availability Zones](./06-Availability-Zones.md)
**Next:** [AWS Management Console](./08-AWS-Management-Console.md)

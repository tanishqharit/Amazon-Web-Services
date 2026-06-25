# AWS Regions

## What is a Region?

A **Region** is a physical location in the world where AWS has a group of data centers.

Think of it like this:
- AWS has "offices" all around the world
- Each office is a **Region**
- Each Region is completely independent

---

## Examples of Regions

| Region Name | Region Code | Location |
|-------------|-------------|----------|
| US East (N. Virginia) | us-east-1 | USA |
| US West (Oregon) | us-west-2 | USA |
| Europe (Ireland) | eu-west-1 | Ireland |
| Asia Pacific (Mumbai) | ap-south-1 | India |
| Asia Pacific (Tokyo) | ap-northeast-1 | Japan |

AWS has **30+ Regions** worldwide.

---

## Why Do Regions Matter?

### 1. Latency (Speed)
- Choose a Region close to your users
- Data travels faster over shorter distances
- User in India → use `ap-south-1` (Mumbai)

### 2. Compliance (Laws)
- Some countries require data to stay within their borders
- Example: EU data must stay in EU Regions (GDPR)

### 3. Service Availability
- Not all AWS services are available in every Region
- New services usually launch in `us-east-1` first

### 4. Pricing
- Prices vary between Regions
- `us-east-1` is usually the cheapest

---

## How to Choose a Region

Ask these questions in order:

1. **Compliance** — Does law require data in a specific location?
2. **Latency** — Where are my users?
3. **Service availability** — Is the service I need available there?
4. **Pricing** — Which region is cheapest?

---

## Key Takeaway

> A Region is a cluster of AWS data centers in a specific geographic location. Choose your Region based on compliance, latency, service availability, and cost.

---

**Previous:** [What is AWS](./04-What-is-AWS.md)
**Next:** [Availability Zones](./06-Availability-Zones.md)

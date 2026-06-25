# AWS Free Tier

## What is the AWS Free Tier?

The **AWS Free Tier** lets you use certain AWS services **for free** — either forever or for 12 months after account creation.

This is great for learning without spending money.

---

## Three Types of Free Tier

| Type | Duration | Example |
|------|----------|---------|
| **Always Free** | Forever | Lambda: 1M free requests/month |
| **12 Months Free** | First year only | EC2: 750 hours/month of t2.micro |
| **Trials** | Short-term | Redshift: 2-month free trial |

---

## Free Tier for Data Engineering Services

| Service | Free Tier |
|---------|-----------|
| **Amazon S3** | 5 GB storage (12 months) |
| **AWS Glue** | No free tier ⚠️ |
| **Amazon Athena** | Pay per query ($5 per TB scanned) |
| **AWS Lambda** | 1 million requests/month (always free) |
| **Amazon DynamoDB** | 25 GB storage (always free) |
| **Amazon Redshift** | 2-month free trial |
| **Amazon Kinesis** | No free tier ⚠️ |
| **Amazon CloudWatch** | 10 custom metrics (always free) |

---

## Tips to Avoid Surprise Bills

1. **Set up billing alerts** — get notified when spending exceeds a threshold
2. **Use AWS Budgets** — set a monthly budget (e.g., $10)
3. **Delete resources after practice** — don't leave services running
4. **Check the billing dashboard** regularly
5. **Use `us-east-1`** — it's usually the cheapest Region

---

## Key Takeaway

> The AWS Free Tier lets you practice for free, but some data engineering services (Glue, Kinesis) are NOT free. Always set up billing alerts and delete resources after learning.

---

**Previous:** [AWS SDKs](./16-AWS-SDKs.md)
**Next:** [Section 02 — What is Data](../02-Data-Engineering-Fundamentals/01-What-is-Data.md)

# Glue Connections

## What is a Glue Connection?

A **Glue Connection** stores the connection details needed to access data sources that are **not in S3** — like databases in a VPC.

---

## When You Need Connections

| Data Source | Needs Connection? |
|-------------|-------------------|
| Amazon S3 | ❌ No (accessed via IAM) |
| Amazon RDS | ✅ Yes (JDBC, inside VPC) |
| Amazon Redshift | ✅ Yes (JDBC) |
| On-premises database | ✅ Yes (JDBC via VPN/Direct Connect) |
| Amazon DynamoDB | ❌ No |

---

## What a Connection Stores

| Property | Example |
|----------|---------|
| Connection type | JDBC, MongoDB, Kafka |
| JDBC URL | `jdbc:mysql://mydb.rds.amazonaws.com:3306/sales` |
| Username/Password | Stored securely (or via Secrets Manager) |
| VPC, Subnet, Security Group | Network configuration |

---

## VPC and Glue

When Glue jobs access resources inside a **VPC** (like RDS), Glue needs:

1. A **VPC connection** configured
2. A **subnet** with available IP addresses
3. A **security group** that allows inbound/outbound traffic
4. A **NAT Gateway or S3 VPC Endpoint** for S3 access from VPC

⚠️ Common exam question: "Glue job can't access S3 from VPC" → need an **S3 VPC Gateway Endpoint**.

---

## Key Takeaway

> Glue Connections store credentials and network info for accessing databases inside VPCs. S3 doesn't need a connection (use IAM). When Glue runs in a VPC, add an S3 VPC endpoint for S3 access.

---

**Previous:** [Glue Triggers](./14-Glue-Triggers.md)
**Next:** [Glue Data Quality](./16-Glue-Data-Quality.md)

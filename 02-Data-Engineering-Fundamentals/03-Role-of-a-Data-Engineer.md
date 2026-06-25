# Role of a Data Engineer

## What Does a Data Engineer Do Day-to-Day?

A data engineer's main job is to make sure **the right data gets to the right people in the right format at the right time**.

---

## Core Responsibilities

### 1. Build Data Pipelines
- Create automated workflows that move data from source → destination
- Example: Customer orders from app → S3 → Glue → Redshift → Dashboard

### 2. Design Data Storage
- Choose the right storage for each use case
- Data lake (S3) vs Data warehouse (Redshift) vs Database (RDS)

### 3. Transform Data
- Clean messy data (remove nulls, fix formats)
- Aggregate data (daily sales totals)
- Join data from multiple sources

### 4. Ensure Data Quality
- Is the data complete?
- Are there duplicates?
- Is the data arriving on time?

### 5. Manage Security
- Who can access what data?
- Is sensitive data encrypted?
- Are there audit logs?

### 6. Monitor and Fix
- Set up alerts when pipelines fail
- Troubleshoot and fix broken pipelines
- Optimize performance and cost

---

## Skills a Data Engineer Needs

| Skill | Why |
|-------|-----|
| SQL | Query and transform data |
| Python | Write ETL scripts and automation |
| Cloud (AWS) | Build and manage infrastructure |
| Data Modeling | Design efficient data structures |
| ETL/ELT | Move and transform data |

---

## Key Takeaway

> A data engineer builds and maintains the systems that make data usable. They design pipelines, choose storage, transform data, ensure quality, and manage security.

---

**Previous:** [What is Data Engineering](./02-What-is-Data-Engineering.md)
**Next:** [What is a Data Pipeline](./04-What-is-a-Data-Pipeline.md)

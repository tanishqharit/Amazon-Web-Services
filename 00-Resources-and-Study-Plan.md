# 📚 AWS Certified Data Engineer – Associate (DEA-C01)

## Resource Guide & Study Plan

---

## 🎯 Exam Overview

| Detail                | Info                                                                 |
| --------------------- | -------------------------------------------------------------------- |
| **Exam Code**         | DEA-C01                                                              |
| **Level**             | Associate                                                            |
| **Questions**         | 65 (50 scored + 15 unscored)                                         |
| **Question Types**    | Multiple-choice & multiple-response                                  |
| **Duration**          | 130 minutes                                                          |
| **Cost**              | $150 USD                                                             |
| **Passing Score**     | 720 / 1000                                                           |
| **Target Experience** | 2–3 years in data engineering on AWS                                 |
| **Delivery**          | Pearson VUE (testing center or online proctored)                     |

---

## 📊 Exam Domains & Weightage

| Domain | Title                             | Weight | Priority |
| ------ | --------------------------------- | ------ | -------- |
| 1      | Data Ingestion and Transformation | **34%** | 🔴 HIGH |
| 2      | Data Store Management             | **26%** | 🔴 HIGH |
| 3      | Data Operations and Support       | **22%** | 🟡 MED  |
| 4      | Data Security and Governance      | **18%** | 🟡 MED  |

> **IMPORTANT:** Domain 1 alone is **34%** of the exam — more than 1 in 3 questions. Master data ingestion (batch + streaming) and transformation (ETL/ELT) first.

---

## 🗂️ Domain Task Statements

### Domain 1: Data Ingestion and Transformation (34%)

| Task | Description |
| ---- | ----------- |
| 1.1  | Perform data ingestion (batch and streaming) |
| 1.2  | Transform and process data |
| 1.3  | Orchestrate data pipelines |
| 1.4  | Apply programming concepts |

**Key Knowledge Areas:**
- Throughput and latency characteristics of ingestion services
- Ingestion patterns (frequency, data history, incremental vs. full load)
- Streaming vs. batch ingestion trade-offs
- Replayability and stateful/stateless data transactions
- Data serialization formats (JSON, CSV, Parquet, ORC, Avro)
- Schema-on-read vs. schema-on-write

---

### Domain 2: Data Store Management (26%)

| Task | Description |
| ---- | ----------- |
| 2.1  | Choose an appropriate data store |
| 2.2  | Understand data cataloging systems |
| 2.3  | Manage the lifecycle of data |

**Key Knowledge Areas:**
- Data lake vs. data warehouse vs. lakehouse architectures
- Storage classes and lifecycle policies (S3)
- Schema design, partitioning, and indexing
- Hot/warm/cold data tiering
- Data retention and archival strategies

---

### Domain 3: Data Operations and Support (22%)

| Task | Description |
| ---- | ----------- |
| 3.1  | Automate data processing by using AWS services |
| 3.2  | Analyze data by using AWS services |
| 3.3  | Maintain and monitor data pipelines |
| 3.4  | Ensure data quality |

**Key Knowledge Areas:**
- Pipeline orchestration and automation
- Performance tuning and cost optimization
- Monitoring, logging, and alerting
- Data validation, profiling, and quality checks
- Troubleshooting failed pipelines

---

### Domain 4: Data Security and Governance (18%)

| Task | Description |
| ---- | ----------- |
| 4.1  | Apply authentication mechanisms |
| 4.2  | Apply authorization mechanisms |
| 4.3  | Ensure data encryption and masking |
| 4.4  | Prepare logs for audit |
| 4.5  | Understand data privacy and governance |

**Key Knowledge Areas:**
- IAM policies, roles, and identity federation
- Row/column/cell-level access control (Lake Formation)
- Encryption at rest (KMS) and in transit (TLS/SSL)
- Data masking, tokenization, PII handling
- CloudTrail for audit logging

---

## 🛠️ In-Scope AWS Services (Organized by Category)

### 🔵 Core Data Engineering (Must Master)

| Service | Role | Priority |
| ------- | ---- | -------- |
| **Amazon S3** | Data lake foundation, object storage | 🔴 Critical |
| **AWS Glue** | ETL/ELT, Data Catalog, Crawlers, DataBrew, Data Quality | 🔴 Critical |
| **Amazon Redshift** | Data warehousing, Spectrum, Federated Query | 🔴 Critical |
| **Amazon Athena** | Serverless SQL analytics on S3 | 🔴 Critical |
| **AWS Lake Formation** | Centralized governance, fine-grained access | 🔴 Critical |

### 🟢 Data Ingestion & Streaming

| Service | Role | Priority |
| ------- | ---- | -------- |
| **Amazon Kinesis Data Streams** | Real-time streaming ingestion | 🔴 Critical |
| **Amazon Kinesis Data Firehose** | Near-real-time delivery to S3/Redshift/OpenSearch | 🔴 Critical |
| **Amazon MSK** | Managed Apache Kafka | 🟡 Important |
| **AWS DMS** | Database migration & CDC (Change Data Capture) | 🟡 Important |
| **AWS DataSync** | Data transfer between on-premises and AWS | 🟡 Important |
| **Amazon AppFlow** | SaaS-to-AWS data integration | 🟢 Know It |

### 🟡 Compute & Processing

| Service | Role | Priority |
| ------- | ---- | -------- |
| **Amazon EMR** | Managed Spark, Hadoop, Hive | 🟡 Important |
| **AWS Lambda** | Serverless event-driven processing | 🟡 Important |
| **Amazon EC2 / ECS / EKS** | Custom compute for processing | 🟢 Know It |

### 🟠 Orchestration & Automation

| Service | Role | Priority |
| ------- | ---- | -------- |
| **AWS Step Functions** | Serverless workflow orchestration | 🟡 Important |
| **Amazon MWAA** | Managed Apache Airflow | 🟡 Important |
| **Amazon EventBridge** | Event-driven architectures | 🟢 Know It |

### 🔴 Databases

| Service | Role | Priority |
| ------- | ---- | -------- |
| **Amazon DynamoDB** | NoSQL, Streams for CDC, DAX | 🟡 Important |
| **Amazon RDS / Aurora** | Managed relational databases | 🟡 Important |
| **Amazon OpenSearch Service** | Search and log analytics | 🟢 Know It |
| **Amazon DocumentDB** | MongoDB-compatible | 🟢 Know It |
| **Amazon Neptune** | Graph database | 🟢 Know It |
| **Amazon Keyspaces** | Cassandra-compatible | 🟢 Know It |

### 🔒 Security, Monitoring & Governance

| Service | Role | Priority |
| ------- | ---- | -------- |
| **AWS IAM** | Identity and access management | 🔴 Critical |
| **AWS KMS** | Encryption key management | 🔴 Critical |
| **Amazon CloudWatch** | Monitoring, logging, metrics, alarms | 🟡 Important |
| **AWS CloudTrail** | API activity logging & audit | 🟡 Important |
| **Amazon Macie** | Sensitive data discovery (PII) | 🟢 Know It |
| **AWS Secrets Manager** | Credential management | 🟢 Know It |

---

## 📖 Study Resources

### 1. 🏛️ Official AWS Resources (Start Here)

| Resource | Description | Cost |
| -------- | ----------- | ---- |
| **AWS Exam Guide (PDF)** | Official exam domains, task statements, in-scope services | Free |
| **AWS Skill Builder — Exam Prep Plan** | Standard course (~6 hours), enhanced course with labs | Free / Subscription |
| **Official Practice Question Set** | 20 free practice questions from AWS | Free |
| **AWS Certification Page** | Latest exam info, registration, and sample questions | Free |
| **AWS Documentation** | Deep-dive reference for each service | Free |
| **AWS Whitepapers** | Architectural best practices and well-architected framework | Free |

**Key Links:**
- Exam Guide: https://d1.awsstatic.com/training-and-certification/docs-data-eng-associate/AWS-Certified-Data-Engineer-Associate_Exam-Guide.pdf
- Skill Builder: https://explore.skillbuilder.aws/
- Certification Page: https://aws.amazon.com/certification/certified-data-engineer-associate/

### 2. 🎓 Online Courses

| Resource | Instructor/Platform | Notes |
| -------- | ------------------- | ----- |
| **Ultimate AWS Certified Data Engineer Associate** | Stephane Maarek (Udemy) | ⭐ Highly recommended by the community; comprehensive coverage |
| **AWS Data Engineer Learning Path** | Pluralsight | Video lessons + labs |
| **AWS Data Analytics Specialization** | Whizlabs | Comprehensive path with practice labs |
| **AWS Data Engineer Bootcamp** | A Cloud Guru | Interactive labs included |

### 3. 📝 Practice Exams (Critical for Exam Readiness)

| Resource | Platform | Notes |
| -------- | -------- | ----- |
| **Tutorials Dojo Practice Exams** | tutorialsdojo.com | ⭐ Most realistic; detailed answer explanations |
| **Skill-cert-pro Practice Tests** | Various | Frequently recommended for realistic mock questions |
| **AWS Official Pre-test** | AWS Skill Builder | Identify knowledge gaps early |
| **Whizlabs Practice Tests** | whizlabs.com | Good supplementary practice |

### 4. 📚 Documentation & Deep-Dives

| Resource | Focus |
| -------- | ----- |
| AWS Glue Developer Guide | ETL, Catalog, Crawlers, Data Quality |
| Amazon Redshift Guide | Warehousing, Spectrum, performance |
| Amazon Kinesis Guides | Streams, Firehose, Analytics |
| Amazon Athena User Guide | Serverless queries, partitioning |
| AWS Lake Formation Guide | Governance, fine-grained access |
| Amazon S3 User Guide | Storage, lifecycle, security |

### 5. 🌐 Community & Supplementary

| Resource | Notes |
| -------- | ----- |
| **r/AWSCertifications (Reddit)** | Real exam experiences, tips, study plans |
| **AWS re:Invent Sessions (YouTube)** | Deep-dive talks on specific services |
| **AWS Data Engineering Blog** | Latest features and best practices |

---

## 📅 Suggested Study Plan (4 Weeks)

### Week 1: Foundations + Domain 1 (Data Ingestion & Transformation)

| Day | Focus Area | Activities |
| --- | ---------- | ---------- |
| 1-2 | **S3 Fundamentals** | Storage classes, lifecycle policies, versioning, encryption, event notifications |
| 3-4 | **AWS Glue Deep Dive** | ETL jobs, Crawlers, Data Catalog, DynamicFrames, job bookmarks, Glue Studio |
| 5   | **Kinesis (Streams + Firehose)** | Shards, partition keys, Firehose delivery, format conversion |
| 6   | **DMS + DataSync + AppFlow** | Migration patterns, CDC, hybrid ingestion |
| 7   | **Review + Practice Questions** | Domain 1 practice tests |

### Week 2: Domain 2 (Data Store Management) + Domain 3 (Operations)

| Day | Focus Area | Activities |
| --- | ---------- | ---------- |
| 1-2 | **Amazon Redshift** | Architecture, distribution styles, sort keys, Spectrum, Federated Query |
| 3   | **Athena + OpenSearch** | SQL on S3, partitioning, Parquet optimization; log analytics |
| 4   | **DynamoDB + RDS/Aurora** | NoSQL patterns, Streams, CDC; relational best practices |
| 5   | **EMR + Lambda** | Spark on EMR, serverless processing |
| 6   | **Step Functions + MWAA** | Pipeline orchestration, DAGs, error handling |
| 7   | **Review + Practice Questions** | Domain 2 & 3 practice tests |

### Week 3: Domain 4 (Security & Governance) + Cross-Domain

| Day | Focus Area | Activities |
| --- | ---------- | ---------- |
| 1-2 | **Lake Formation** | Fine-grained access, cross-account sharing, tag-based access |
| 3   | **IAM + KMS** | Policies, roles, encryption strategies |
| 4   | **CloudWatch + CloudTrail** | Monitoring pipelines, audit logging |
| 5   | **Macie + Secrets Manager** | PII detection, credential management |
| 6-7 | **End-to-End Architecture** | Build a mental model: Ingest → Transform → Store → Govern → Analyze |

### Week 4: Practice & Review

| Day | Focus Area | Activities |
| --- | ---------- | ---------- |
| 1-2 | **Full Practice Exams** | Tutorials Dojo / Skill-cert-pro |
| 3-4 | **Review Weak Areas** | Re-study services where you scored lowest |
| 5   | **Full Practice Exam** | Timed simulation under exam conditions |
| 6   | **Final Review** | Cheat sheets, flashcards, quick-reference notes |
| 7   | **🎯 EXAM DAY** | You got this! 🚀 |

---

## 📂 Notes Structure (What We'll Build)

Below is the folder structure for the notes we'll create together. Each file will be a comprehensive, exam-focused markdown document:

```
AWS/
├── 00-Resources-and-Study-Plan.md          ← 📍 You are here
│
├── 01-Data-Ingestion-and-Transformation/   ← Domain 1 (34%)
│   ├── 01-Amazon-S3.md
│   ├── 02-AWS-Glue.md
│   ├── 03-Amazon-Kinesis.md
│   ├── 04-AWS-DMS.md
│   ├── 05-AWS-Lambda.md
│   ├── 06-Data-Formats-and-Serialization.md
│   └── 07-Batch-vs-Streaming-Patterns.md
│
├── 02-Data-Store-Management/               ← Domain 2 (26%)
│   ├── 01-Amazon-Redshift.md
│   ├── 02-Amazon-Athena.md
│   ├── 03-Amazon-DynamoDB.md
│   ├── 04-Amazon-RDS-Aurora.md
│   ├── 05-Amazon-OpenSearch.md
│   ├── 06-Data-Lake-vs-Warehouse-vs-Lakehouse.md
│   └── 07-Data-Modeling-and-Partitioning.md
│
├── 03-Data-Operations-and-Support/         ← Domain 3 (22%)
│   ├── 01-AWS-Step-Functions.md
│   ├── 02-Amazon-MWAA.md
│   ├── 03-Amazon-EMR.md
│   ├── 04-Amazon-CloudWatch.md
│   ├── 05-Pipeline-Orchestration-Patterns.md
│   └── 06-Cost-Optimization.md
│
├── 04-Data-Security-and-Governance/        ← Domain 4 (18%)
│   ├── 01-AWS-Lake-Formation.md
│   ├── 02-AWS-IAM-for-Data-Engineering.md
│   ├── 03-AWS-KMS-Encryption.md
│   ├── 04-CloudTrail-Auditing.md
│   ├── 05-Amazon-Macie.md
│   └── 06-Data-Privacy-and-Compliance.md
│
└── 05-Exam-Tips/
    ├── 01-Service-Comparison-Cheat-Sheet.md
    ├── 02-Architecture-Patterns.md
    └── 03-Common-Exam-Scenarios.md
```

---

## 🧠 Exam Strategy Tips

1. **Eliminate Wrong Answers** — Most questions have 1-2 obviously wrong choices. Narrow down first.
2. **Look for Keywords** — "Real-time" → Kinesis Streams; "Near-real-time" → Firehose; "Serverless" → Athena/Glue/Lambda; "Cost-effective" → S3 + Athena.
3. **"Most" Qualifiers** — "Most cost-effective", "Most operationally efficient", "Least effort" — these hint at managed/serverless solutions.
4. **Understand Trade-offs** — Kinesis vs. MSK, Glue vs. EMR, Redshift vs. Athena — the exam loves "when to pick what."
5. **Security Is Everywhere** — Even in Domain 1-3 questions, expect security aspects (encryption, IAM roles, VPC).
6. **Don't Over-Engineer** — AWS favors simple, managed, serverless solutions. If two options work, pick the one with less operational overhead.

---

> **Next Step:** Tell me which topic or domain you'd like to start with, and I'll begin writing detailed, exam-focused notes! I recommend starting with **Domain 1 (Data Ingestion & Transformation)** since it's the highest-weighted at 34%.

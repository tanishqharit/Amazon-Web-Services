# Glue Workflows

## What is a Glue Workflow?

A **Glue Workflow** lets you orchestrate multiple Glue components (crawlers, jobs, triggers) into a **single, coordinated pipeline**.

---

## How It Works

```
Workflow: Daily Sales Pipeline
├── Step 1: Crawler scans new S3 data
├── Step 2: ETL Job transforms data (depends on Step 1)
├── Step 3: Another ETL Job loads to Redshift (depends on Step 2)
└── Step 4: Crawler updates processed table (depends on Step 3)
```

---

## Components in a Workflow

| Component | Role |
|-----------|------|
| **Triggers** | Start the workflow (schedule, on-demand, or event) |
| **Crawlers** | Discover schemas |
| **Jobs** | Transform data |
| **Conditions** | Control flow based on success/failure |

---

## Workflow vs Step Functions

| Feature | Glue Workflows | Step Functions |
|---------|---------------|----------------|
| Scope | Glue-only components | Any AWS service |
| Complexity | Simple chains | Complex branching, parallel |
| Monitoring | Glue console | Step Functions console |
| Use when | All steps are Glue | Mix of services |

---

## Key Takeaway

> Glue Workflows chain crawlers, jobs, and triggers into a coordinated pipeline within Glue. For simple Glue-only pipelines, use Workflows. For complex multi-service orchestration, use Step Functions or MWAA.

---

**Previous:** [Glue DataBrew](./12-Glue-DataBrew.md)
**Next:** [Glue Triggers](./14-Glue-Triggers.md)

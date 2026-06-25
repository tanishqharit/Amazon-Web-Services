# Glue DataBrew

## What is Glue DataBrew?

**AWS Glue DataBrew** is a **visual data preparation tool** for cleaning and normalizing data — without writing code. It's designed for **analysts** and **non-programmers**.

---

## DataBrew vs Glue ETL Jobs

| Feature | DataBrew | Glue ETL Jobs |
|---------|----------|---------------|
| **Target user** | Analysts, non-coders | Developers, data engineers |
| **Interface** | Visual, point-and-click | Code (PySpark/Scala) |
| **Complexity** | Simple transformations | Complex transformations |
| **Over 250 built-in transforms** | ✅ Yes | Write custom code |
| **Data profiling** | ✅ Built-in | Manual |

---

## Key Features

- **250+ built-in transformations** — no code needed
- **Data profiling** — automatically analyze data quality, distributions, patterns
- **Recipes** — save and reuse transformation steps
- **Dataset preview** — see the effect of each transformation instantly

---

## Common Transformations

- Remove duplicates
- Fix date formats
- Handle missing values
- Split/merge columns
- Filter rows
- Convert data types

---

## When to Use DataBrew

- Quick data cleaning by **non-technical users**
- **Data profiling** (understand data quality before ETL)
- Simple transformations that don't need custom code

---

## Key Takeaway

> DataBrew is a visual, no-code data cleaning tool with 250+ built-in transforms. Use it for data profiling and simple data preparation. For complex ETL, use Glue Spark jobs.

---

**Previous:** [Glue Studio](./11-Glue-Studio.md)
**Next:** [Glue Workflows](./13-Glue-Workflows.md)

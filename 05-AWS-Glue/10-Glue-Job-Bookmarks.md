# Glue Job Bookmarks

## What are Job Bookmarks?

**Job Bookmarks** track which data has already been processed so that Glue jobs only process **new data** on each run.

Without bookmarks: Every run processes ALL data (wasteful, slow).
With bookmarks: Each run processes only NEW data (efficient, fast).

---

## How It Works

```
Run 1: Process files 1-100     → Bookmark saves: "processed up to file 100"
Run 2: Process files 101-150   → Bookmark saves: "processed up to file 150"
Run 3: Process files 151-200   → Bookmark saves: "processed up to file 200"
```

---

## Supported Sources

- **Amazon S3** — tracks by file timestamp/path
- **JDBC sources** — tracks by primary key or timestamp column
- **Relational databases** — RDS, Aurora

---

## Bookmark Options

| Option | Behavior |
|--------|----------|
| **Enable** | Process only new data |
| **Disable** | Process all data every run |
| **Pause** | Keep bookmark state but don't update it |

---

## For the Exam

Keyword: **"Incremental processing"** or **"avoid reprocessing"** → **Job Bookmarks**

If the question says "process only new data" → enable Job Bookmarks.

---

## Key Takeaway

> Job Bookmarks let Glue jobs process only new data, avoiding reprocessing. Enable them for incremental ETL. They work with S3 and JDBC sources.

---

**Previous:** [Glue DynamicFrames](./09-Glue-DynamicFrames.md)
**Next:** [Glue Studio](./11-Glue-Studio.md)

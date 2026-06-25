# OLTP Explained

## What is OLTP?

**OLTP (Online Transaction Processing)** is a system designed to handle **many small, fast transactions**.

Think of it like a cash register at a store:
- Each purchase is a **transaction**
- You need it to be **fast** (customer is waiting)
- You do **one operation at a time** (insert, update, delete)

---

## Characteristics

| Feature | OLTP |
|---------|------|
| **Purpose** | Handle transactions |
| **Operations** | INSERT, UPDATE, DELETE (one row at a time) |
| **Speed** | Very fast for individual operations |
| **Data size** | Small per transaction |
| **Users** | Applications, end users |
| **Example** | Online shopping cart, bank transfer |

---

## OLTP Example

```sql
-- A customer places an order (OLTP transaction)
INSERT INTO orders (customer_id, product, quantity, total)
VALUES (123, 'Laptop', 1, 75000);
```

This is fast, affects one row, and is done millions of times a day.

---

## AWS Services for OLTP

| Service | Type |
|---------|------|
| **Amazon RDS** | Managed relational database |
| **Amazon Aurora** | High-performance relational database |
| **Amazon DynamoDB** | NoSQL database for fast transactions |

---

## Key Takeaway

> OLTP handles fast, small transactions (like purchases and sign-ups). RDS, Aurora, and DynamoDB are AWS OLTP services.

---

**Previous:** [Data Lake vs Data Warehouse](./17-Data-Lake-vs-Data-Warehouse.md)
**Next:** [OLAP Explained](./19-OLAP-Explained.md)

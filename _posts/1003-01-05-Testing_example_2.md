---
layout: post
---

## Example
```yml
version: 2

models:
  - name: customers
    columns:
      - name: customer_id
        tests:
          - not_null
          - unique

```
```sql

select count(*) from (
  select
    customer_id

  from analytics.customers
  group by customer_id
  having count(*) > 1
)

```


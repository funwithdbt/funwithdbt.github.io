---
layout: post
---

## Why might a test fail ?

```sql
select
    customers.customer_id,
    customer_orders.number_of_orders
from customers

left join customer_orders using (customer_id)

```

```yml
version: 2

models:
  - name: customers
    columns:
      - name: number_of_orders
        tests:
          - not_null
```
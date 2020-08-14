---
layout: post
---

## Why might a test fail ??

1. The SQL in your model doesn’t do what you intended.

```sql
select
    customers.customer_id,
    coalesce(customer_orders.number_of_orders, 0) as number_of_orders
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



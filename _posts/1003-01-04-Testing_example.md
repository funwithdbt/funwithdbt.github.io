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

```
= 

```sql

select
  count(*)

from analytics.customers
where customer_id is null
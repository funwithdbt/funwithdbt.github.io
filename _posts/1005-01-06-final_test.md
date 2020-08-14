---
layout: post
---

## Custom Tests

`tests/refund_cannot_exceed_amount.sql`
```sql
-- refunds have a negative amount, so the total amount should always be > 0
select
    order_id,
    sum(amount) as total_amount

from {{ ref('fct_payments' )}}

group by 1

having total_amount < 0
```

---
layout: post
---

## Analyses

_'analysis/mrr_dashboard.sql'_

```sql
select
    date_month,

    sum(is_active::integer) as customers,
    sum(mrr) as mrr

from {{ ref('fct_mrr') }}

group by 1
```
.caption[
[Analyses](https://docs.getdbt.com/docs/analyses)
]
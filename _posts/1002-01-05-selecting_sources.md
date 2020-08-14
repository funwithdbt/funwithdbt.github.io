---
layout: post
---

## Selecting from sources

Use the _{{ source() }}_ function to select from a source in a model:

```sql
with source as (

    select * from {{ source('jaffle_shop', 'customers') }}

),

```



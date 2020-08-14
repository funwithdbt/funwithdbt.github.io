---
layout: post
---

# Selecting from sources

Use the `{{ source() }}` function to select from a source in a model:

.left-column[

```sql
with source as (

    select * from {{ source('jaffle_shop', 'customers') }}

),

renamed as (

...
```



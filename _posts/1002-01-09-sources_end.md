---
layout: post
---

## Sources 
Given the following YML file, what will the following select statements compile to?

.left-column[
`sources.yml`
```yml
version: 2

sources:
  - name: snowplow
    database: raw
    tables:
      - name: events
  - name: stripe
    database: raw
    tables:
      - name: payments
```
`SQL`
```sql
select *
from {{ source('stripe','payments') }}
```


```sql
select *
from {{ source('snowplow', 'events') }}
```



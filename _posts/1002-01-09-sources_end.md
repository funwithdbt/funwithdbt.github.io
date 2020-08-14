---
layout: post
---

## Sources 
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
```sql
select *
from {{ source('stripe','payments') }}
```
```sql
select *
from {{ source('snowplow', 'events') }}
```



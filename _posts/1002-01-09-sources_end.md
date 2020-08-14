---
layout: post
---

## Checkpoint
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
]


.right-column[
`SQL`
```sql
select *
from {{ source('stripe','payments') }}
```


```sql
select *
from {{ source('snowplow', 'events') }}
```
]



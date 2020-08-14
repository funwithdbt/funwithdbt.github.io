---
layout: post
---

## Testing sources

.denser-text[

Sources as well !! wow !!
]

.denser-text[
```yml
version: 2

sources:
  - name: jaffle_shop
    database: raw
    tables:
      - name: customers
        columns:
          - name: id
            tests:
              - not_null
              - unique
```
]



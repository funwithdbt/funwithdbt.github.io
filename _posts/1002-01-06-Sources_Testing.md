---
layout: post
---

## Testing sources

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



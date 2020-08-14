---
layout: post
---

## Defining sources
Sources are defined in `.yml` files in `models/` dir.

```yml
version: 2

sources:
  - name: jaffle_shop
    database: raw
    tables:
      - name: customers
      - name: orders

```



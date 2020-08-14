---
layout: post
---

## Defining sources
Sources are defined in `.yml` files in your `models/` directory.

(They can co-exist with `models:` blocks)

```yml
version: 2

sources:
  - name: jaffle_shop
    database: raw
    tables:
      - name: customers
      - name: orders

```



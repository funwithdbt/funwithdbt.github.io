---
layout: post
---

## Feeling fresh?
`loaded_at_field` and `freshness`:

```yml
version: 2

sources:
  - name: jaffle_shop
    database: raw

    tables:
      - name: customers

      - name: orders
        loaded_at_field: _etl_loaded_at

        freshness:
          warn_after: {count: 12, period: hour}
          error_after: {count: 24, period: hour}

```
Then run `dbt source snapshot-freshness`



---
layout: post
---

```bash
$ dbt run-operation grant_select
```

```yml
version: 2

models:
  - name: dim_customers
    columns:
      - name: customer_id
        tests:
          - unique:
              error_threshold: 10
```
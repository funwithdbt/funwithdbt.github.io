---
layout: post
---

## Builtins

* `unique`
* `not_null`
* **`accepted_values`**
* `relationships`

```yml
version: 2

models:
  - name: orders
    columns:
      - name: status
        tests:
          - accepted_values:
              values: ['placed', 'shipped', 'completed', 'returned']
```


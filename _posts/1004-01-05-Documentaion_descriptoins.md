---
layout: post
---

## Documentation

```yml
version: 2

models:
  - name: orders
    description: One record per order
    columns:
      - name: order_id
        tests:
          - unique
          - not_null

      - name: status
        description: "{{ doc('order_status') }}"
        tests:
          - accepted_values:
              values: ['placed', 'shipped', 'completed', 'return_pending', 'returned']

      - name: amount
        description: Amount in USD
```

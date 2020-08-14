---
layout: post
---

## Additional Features
❓ How do I make my data immutable?

| order_id | status  | updated_at | dbt_valid_from | dbt_valid_to |
|----------|---------|------------|----------------|--------------|
| 1        | pending | 2019-01-01 | 2019-01-01     | 2019-01-02   |
| 1        | shipped | 2019-01-02 | 2019-01-02     | null         |


✅ Technique: Snapshots

```bash
$ dbt snapshot
```


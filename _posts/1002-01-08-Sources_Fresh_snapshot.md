---
layout: post
---

## Snapshotting freshness

```yml
$ dbt source snapshot-freshness
Running with dbt=0.16.0
Found 5 models, 20 tests, 0 snapshots, 0 analyses, 130 macros, 0 operations, 0 seed files, 3 sources

17:29:17 | Concurrency: 4 threads (target='learn')
17:29:17 |
17:29:17 | 1 of 1 START freshness of jaffle_shop.orders......................... [RUN]
17:29:20 | 1 of 1 WARN freshness of jaffle_shop.orders.......................... [WARN in 2.91s]
17:29:21 | Done.
```

😀

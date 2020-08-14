---
layout: post
---

## In deployment

A common approach: Test the schema integrity of raw tables _before_
replacing production models.

```bash
dbt test -m source:*            # ensure no duplicates or unexpected nulls -- the job won't continue if these tests fail
dbt run                         # only runs if test above succeeds
dbt test --exclude source:*     # or you can even skip these!
dbt source snapshot-freshness   # powers freshness viz in dbt Cloud
```

Alternate: `snapshot-freshness` first, so that job won't run on stale data.



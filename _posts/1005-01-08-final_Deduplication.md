---
layout: post
---

## Deduplication

  ```sql
  select
    *,
    row_number() over (
        partition by user_id
        order by created_at desc
    ) = 1 as is_most_recent_record
  from users
  qualify is_most_recent_record



  ```
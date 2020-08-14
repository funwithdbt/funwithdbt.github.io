---
layout: post
---
## Materializations

--
* `materializations` are build strategies
* i.e. the SQL that your `select` statement gets wrapped in
* Models can be materialized as `views` and `tables` (we'll learn more later!)
* You need to **configure** a model's materialization
* If you weren't using dbt, this would look like writing a lot of DDL in the
Snowflake console



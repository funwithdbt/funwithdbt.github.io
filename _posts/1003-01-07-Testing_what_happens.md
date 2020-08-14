---
layout: post
---

###  `dbt test` ?

1. dbt connection to your **data warehouse** (via a **profile/connection**)
2. dbt parses your **dbt project**
3. dbt iterates through the resource files (`models/**.yml`) to construct `select` queries.
4. dbt executes the SQL for each test: if the number `0` is returned your test passes*
---
layout: post
---

## Operations

A _macro_ that you can run using the _run-operation_ command

```sql
-- macros/grant_select.sql
{% macro grant_select() %}
{% set grant_sql %}
grant usage on schema {{ target.schema }} to role reporter;
grant select on dbt_claire.customers to role reporter;
{% endset %}
{% do run_query(grant_sql) %}
{% endmacro %}

```

Command line:
```bash
$ dbt run-operation grant_select
```
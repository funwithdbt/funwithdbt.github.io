---
layout: post
---

A that you can run using the run-operation command

```sql
-- macros/grant_select.sql
{% macro grant_select() %}
{% set grant_sql %}
grant usage on schema {{ target.schema }} to role reporter;
grant select on dbt_claire.customers to role reporter;
{% endset %}
{% do run_query(grant_sql) %}
{% endmacro %}
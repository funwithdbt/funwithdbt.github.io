## Notes

# What happens when you `dbt run`?
1. dbt connects to your **data warehouse** (via a **profile**/**connection**)
2. dbt parses your **dbt project**
3. dbt wraps your **models** in the appropriate DDL/DML (e.g. `create table as`)
4. dbt executes this code to build your models in your **target schema**
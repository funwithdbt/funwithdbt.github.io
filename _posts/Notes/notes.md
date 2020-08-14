## Notes

# What happens when you `dbt run`?
1. dbt connects to your **data warehouse** (via a **profile**/**connection**)
2. dbt parses your **dbt project**
3. dbt wraps your **models** in the appropriate DDL/DML (e.g. `create table as`)
4. dbt executes this code to build your models in your **target schema**


dbt (data build tool) enables analytics engineers to transform data in their warehouses by simply writing select statements. dbt handles turning these select statements into tables and views.

dbt does the T in ELT (Extract, Load, Transform) processes – it doesn’t extract or load data, but it’s extremely good at transforming data that’s already loaded into your warehouse.

The role of dbt within a modern data stack is discussed in more detail here.

dbt also enables analysts to work more like software engineers, in line with the dbt Viewpoint.

dbt handles boilerplate code to materialize queries as relations.

Documentation

Tests

Package management: 

Data snapshots:

Understand raw data sources:

who should used it ?

 It can be used by data engineers, data analysts and data scientists, or anyone that knows how to write select queries in SQL.


dbt run

dbt test

dbt test -m specific_model

dbt source snapshot-freshness

dbt docs generate

dbt run --models stg_customers

dbt test -m stg_orders
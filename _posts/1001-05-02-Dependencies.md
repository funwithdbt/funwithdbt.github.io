---
layout: post
---
##  Creating dependencies  
* Use the `ref` function to do build dependencies between models
* The `ref` function _also_ compiles to the full table/view name, using the correct schema for your environment
* These dependencies form a **Directed Acyclic Graph (DAG)**
* dbt uses this DAG to understand the order to run models in
* This makes it easy to split long queries up into separate models


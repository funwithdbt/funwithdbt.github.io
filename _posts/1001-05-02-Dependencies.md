---
layout: post
---
##  Creating dependencies  
*  `ref` function to do build dependencies
* The `ref` function _also_ compiles to the full table/view name, using the correct schema for your environment
* These dependencies form a **(DAG)**
* dbt uses DAG to understand the order to run models
* easy to split long queries up into separate models


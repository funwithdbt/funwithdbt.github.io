---
layout: post
---
##  Configurations

--
* `configurations` are model settings
* They can be set in your `dbt_project.yml` file, _and_ in your model file.
* Configurations are applied _hierarchically_
* Example configurations:
    * `materialized='view'`
    * `tags=['nightly', 'hourly']`
    * `enabled=True`


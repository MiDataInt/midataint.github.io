---
title: By Category
parent: Tool Suite Registry
has_children: false
nav_order: 10
---


{% for provider_hash in site.data.registry %}
{% assign provider = provider_hash[1] %}
- {{ provider.github_name }}
{% unless provider.github_name == "_templateUser" %}
- IS OK
{% endunless %}
{% endfor %}

<!-- <pre>_template{
    "github_name"=>"_templateUser", 
    "suites"=>[{
        "name"=>"suite_1", 
        "description"=>"suite description #1", 
        "category"=>"Category [: Subcategory]", 
        "pipelines"=>[{"name"=>"pipeline_1",  "description"=>"Stage 1 Pipeline description #1"}], 
        "shared_modules"=>[{"name"=>"path/to/module_1", "description"=>"shared module description #1"}], 
        "apps"=>[{"name"=>"app_1", "description"=>"Stage 2 App description #1"}]
    }]
}</pre> -->

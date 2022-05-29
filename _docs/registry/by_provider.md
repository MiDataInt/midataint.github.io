---
title: By Category
parent: Tool Suite Registry
has_children: false
nav_order: 10
---


{% for provider_hash in site.data.registry %}
    <p>{{ provider_hash.github_name }}</p>
    {% unless provider_hash.github_name == "_templateUser" %}
        <p>IS OK</p>
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


<!-- _template{"github_name"=>"abc123", "suites"=>[{"name"=>"suite_1", "description"=>"suite description #1", "category"=>"Category [: Subcategory]", "pipelines"=>[{"name"=>"pipeline_1", "description"=>"Stage 1 Pipeline description #1"}], "shared_modules"=>[{"name"=>"path/to/module_1", "description"=>"shared module description #1"}], "apps"=>[{"name"=>"app_1", "description"=>"Stage 2 App description #1"}]}]} -->

<!-- provider.github_name == _templateUser -->

---
title: cv
layout: default
---

# Education

<ul>
{% for entry in site.data.education %}
    <school>
        <schoolname>{{ entry.where }}</schoolname>
        <degree>{{ entry.what }}</degree>
        <degreedesc>{{ entry.misc }}</degreedesc>
    </school>
    <when>{{ entry.when }}</when> <br/>
{% endfor %}
</ul>

# Publications

{% for publication in site.data.papers %}
<pubtitle> <a href="http://dx.doi.org/{{publication.DOI}}"> {{ publication.title }} </a> <br/></pubtitle>

<authors>
{%if publication.author.size < 5 %}

{% for author in publication.author %} {{author.given}} {{author.family}} {% endfor %} {{ publication.DOI }}

{% else %}

{% for author in publication.author%}
    {%if forloop.index < 5 %}
        {{author.given}} {{author.family}},
    {% endif %}
{% endfor %}

...,

{{publication.author.last.given}} {{publication.author.last.family}}.


{% endif %}

</authors>

<publisher> {{ publication.publisher }} </publisher>

{% endfor %}


# Experience

<ul>
{% for entry in site.data.experience %}
    <job>
    <left>
        <employer>{{ entry.where }}</employer>
        <jobtitle>{{ entry.what }}</jobtitle>
        <jobdesc>{{ entry.misc }}</jobdesc>
    </left>

    <when>{{ entry.when }}</when>


    </job>

{% endfor %}
</ul>

# Skills

## Programming
<div>
{% for entry in site.data.skills.programming.fluent %}
 {{ entry }},
{% endfor %}
</div>

<ul>
{% for entry in site.data.skills.programming.proficient %}
    <li>
    <place>{{ entry }} </place>
    </li>
{% endfor %}
</ul>

## Data science and visualization
<ul>
{% for entry in site.data.skills.datascience %}
    <li>
    {{ entry }}
    </li>
{% endfor %}
</ul>

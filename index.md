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

# Experience

<ul>
{% for entry in site.data.experience %}
    <job>
        <employer>{{ entry.where }}</employer>
        <jobtitle>{{ entry.what }}</jobtitle>
        <jobdesc>{{ entry.misc }}</jobdesc>
    </job>
    <when>{{ entry.when }}</when>
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
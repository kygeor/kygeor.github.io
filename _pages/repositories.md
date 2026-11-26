---
layout: page
permalink: /repositories/
title: repositories
description: code accompanying my papers. Everything is on <a href="https://github.com/kygeor">GitHub</a>.
nav: true
nav_order: 5
---

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}

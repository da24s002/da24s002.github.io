---
layout: page
permalink: /repositories/
title: repositories
description: ""
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub users

<div class="repositories d-flex flex-column w-100 py-2">
  {% for user in site.data.repositories.github_users %}
    <div class="py-2 border-bottom">
      <a href="https://github.com/{{ user }}" target="_blank" rel="noopener noreferrer" class="repo-user-link" style="color: var(--global-theme-color); text-decoration: underline; font-size: 1.2rem; font-weight: 500;">
        {{ user }} ↗
      </a>
    </div>
  {% endfor %}
</div>
{% endif %}

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}

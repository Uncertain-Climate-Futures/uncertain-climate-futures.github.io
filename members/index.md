---
layout: single
title: "Group Members"
permalink: /members/
author_profile: false
classes: members-directory
---

Our group consists of a steering committee and a broad network of researchers.

{% for group in site.data.members %}
<section aria-labelledby="{{ group.title | slugify }}">
  <h2 id="{{ group.title | slugify }}">
    {% if group.url %}
      <a href="{{ group.url | relative_url }}">{{ group.title | escape }}</a>
    {% else %}
      {{ group.title | escape }}
    {% endif %}
  </h2>
  <ul class="members-grid" role="list">
    {% for member in group.members %}
    <li class="members-grid__person">
      <strong>
        {% if member.website %}
          <a href="{{ member.website | escape }}">{{ member.name | escape }}</a>
        {% else %}
          {{ member.name | escape }}
        {% endif %}
      </strong>
      <span class="members-grid__affiliation">{{ member.affiliation | escape }}</span>
    </li>
    {% endfor %}
  </ul>
</section>
{% endfor %}

*Last updated: October 2026*

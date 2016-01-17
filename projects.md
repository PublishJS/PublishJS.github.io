---
layout: page
title: Projects
category-list: [hyphenation, typography, epub, interactive, charts]
---

[blog](http://www.publishjs.io) [projects](http://publishjs.io/projects)

<p class="message">
  Hey there! This page is included as an example. Feel free to customize it for your own use upon downloading. Carry on!
</p>
{% for cat in site.category-list %}
### {{ cat  }}
<ul>
  {% for page in site.pages %}
    {% if page.projects == true %}
      {% for pc in page.categories %}
        {% if pc == cat %}
          <li><a href="{{ page.url  }}">{{ page.title  }}</a> - <small>{{ page.description }}</small></li>
        {% endif %}   <!-- cat-match-p -->
      {% endfor %}  <!-- page-category -->
    {% endif %}   <!-- projects-p -->
  {% endfor %}  <!-- page -->
</ul>
{% endfor %}  <!-- cat -->

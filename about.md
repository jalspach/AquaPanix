---
layout: default
---
## Me
Not much exciting here...just a nerd who likes playing with systems.
<hr>
<nav>
  {% for item in site.data.navigation %}
    <a href="{{ item.link }}" {% if page.url == item.link %}style="color: red;"{% endif %}>
      {{ item.name }}
    </a>
  {% endfor %}
</nav>

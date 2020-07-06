## Why
This site will be my notes on this initial Aquaponics project, hopefully, it will help someone else get started or avoid some things I have accidentally done. I will try to break down the costs and what I have done each day along with what I wish I would have done.
It is also a fun way to play with [Jekyll](https://jekyllrb.com/), GitHub and a few other tools.

For a look at the electronics I hope to someday incorporate, you can check out my [TechList](/AquaPanix/TechList.md) page.

<nav>
  {% for item in site.data.navigation %}
    <a href="{{ item.link }}" {% if page.url == item.link %}style="color: red;"{% endif %}>
      {{ item.name }}
    </a>
  {% endfor %}
</nav>

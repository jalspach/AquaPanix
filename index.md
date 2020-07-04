## Why
This site will act as my notes on my Aquaponics project, hopefully, will help someone else someday. I will try to break down the costs and what I have done each day along with what I wish I would have done.



<nav>
  {% for item in site.data.navigation %}
    <a href="{{ item.link }}" {% if page.url == item.link %}style="color: red;"{% endif %}>
      {{ item.name }}
    </a>
  {% endfor %}
</nav>

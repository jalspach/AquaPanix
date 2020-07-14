---
layout: default
---
This site is dedicated to keeping my notes about what I have done setting up an Aquaponics system in my backyard. There are a million ways to do that and many of them are better than what I have done. However, I had to start somewhere and this is where I started :-)

These notes will help me and I move along. I can keep track of ideas and costs and reasons for different things. In a perfect world, it will also help someone else some day since they can see where I have been and use it as a jumping off place.

Finally...this is a great way to play with Jekell and github.

<hr>
<nav>
  {% for item in site.data.navigation %}
    <a href="{{ item.link }}" {% if page.url == item.link %}style="color: red;"{% endif %}>
      {{ item.name }}
    </a>
  {% endfor %}
</nav>

---
layout: default
---
Below is a list of parts that I have used so far. I will try to keep this updated as times goes on. There should be enough info here to replicate exactly what I have.

## Parts List
<table>
  {% for row in site.data.AquaPanixParts %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>

### Tools List
<table>
  {% for row in site.data.AquaPanixTools %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>

---
layout: page
title: Participants
participants:
  - {name: Max Horn, affiliation: University of Kaiserslautern-Landau, Germany}

  - {name: Iryna Raievska, affiliation: University of Warsaw, Warsaw, Poland; Institute of Mathematics of National Academy of Sciences of Ukraine, Kyiv, Ukraine

  - {name: Maryna Raievska, affiliation: University of Warsaw, Warsaw, Poland; Institute of Mathematics of National Academy of Sciences of Ukraine, Kyiv, Ukraine

---

<ol>{% assign participants = page.participants | sort: "name" %}
{% for p in participants %}
  <li>
    <strong>{{ p.name }}</strong>
    {% if p.affiliation != null %} ({{ p.affiliation }}){% endif %}
    {% if p.links != null %}
        {% for item in p.links %}
            <a href="{{ item[1] }}">({{ item[0] }})</a>
        {% endfor %}
    {% endif %}
    <br/>
      {% if p.talk != null %} Talk: {{ p.talk }}{% endif %}
  </li>
{% endfor %}
</ol>

{% if site.data.feedback.size > 0 %}

<ul>
{% for p in site.data.feedback %}
  <li>
    <strong>{{ p.name }}</strong>
    {% if p.package != null %} (author of {{ p.package }}){% endif %}
    <br/>
    {% if p.feedback != null %} {{ p.feedback }}{% endif %}
  </li>
{% endfor %}
</ul>

{% endif %}

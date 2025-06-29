---
layout: page
title: Participants
participants:
  - {name: Bettina Eick, affiliation: "TU Braunschweig, Germany"}
  - {name: István Szöllősi, affiliation: "Babeș-Bolyai University, Romania"}
  - {name: Jan De Beule, affiliation: "Vrije Universiteit Brussel, Belgium"}
  - {name: Leonard Soicher, affiliation: "Queen Mary University of London, U.K."}
  - {name: Lukas Schnelle, affiliation: "RWTH Aachen University, Germany"}
  - {name: Max Horn, affiliation: "RPTU Kaiserslautern-Landau University, Germany"}
  - {name: Meike Weiß, affiliation: "RWTH Aachen University, Germany"}
  - {name: Michel Lavrauw, affiliation: "University of Primorska, Slovenia"}
  - {name: Óscar Fernández Ayala, affiliation: "TU Braunschweig, Germany"}
  - {name: Rhys Evans, affiliation: "IMFM, Slovenia"}
  - {name: Russ Woodroofe, affiliation: "University of Primorska, Slovenia"}
---

<ol>{% assign participants = page.participants %}
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

<!--
## Conference photo
[<img src="{{ site.baseurl }}/public/conf_photo.jpg" />]({{ site.baseurl }}/public/conf_photo.jpg)
-->

---
layout: page
title: Participants
participants:
  - {name: Andrea Švob, affiliation: "University of Rijeka, Croatia"}
  - {name: Antonio Montero, affiliation: "University of Ljubljana, Slovenia"}
  - {name: Bernhard Böhmler, affiliation: "Leibniz University Hannover"}
  - {name: Bettina Eick, affiliation: "TU Braunschweig, Germany"}
  - {name: Bojan Kuzma, affiliation: "University of Primorska, Slovenia"}
  - {name: Charles Leedham-Green (online), affiliation: "Queen Mary University of London, U.K."}
  - {name: Cheryl Praeger (online), affiliation: "University of Western Australia, Australia"}
  - {name: Dean Crnković, affiliation: "University of Rijeka, Croatia"}
  - {name: Frank Lübeck, affiliation: "RWTH Aachen University, Germany"}
  - {name: George Savvoudis, affiliation: "University of Primorska, Slovenia"}
  - {name: Giusy Monzillo, affiliation: "University of Primorska, Slovenia"}
  - {name: Henrik Schanze, affiliation: "TU Braunschweig, Germany"}
  - {name: István Szöllősi, affiliation: "Babeș-Bolyai University, Romania"}
  - {name: James Mitchell, affiliation: "University of St Andrews, U.K."}
  - {name: Joseph Edwards, affiliation: "University of St Andrews, U.K."}
  - {name: Leonard Soicher, affiliation: "Queen Mary University of London, U.K."}
  - {name: Leonid Ovchinnikov, affiliation: "University of Primorska, Slovenia"}
  - {name: Leyla Işık, affiliation: "University of Primorska, Slovenia"}
  - {name: Lukas Schnelle, affiliation: "RWTH Aachen University, Germany"}
  - {name: Max Horn, affiliation: "RPTU Kaiserslautern-Landau University, Germany"}
  - {name: Meike Weiß, affiliation: "RWTH Aachen University, Germany"}
  - {name: Michel Lavrauw, affiliation: "University of Primorska, Slovenia"}
  - {name: Milad Ahanjideh, affiliation: "University of Primorska, Slovenia"}
  - {name: Morgan Rodgers, affiliation: "RPTU Kaiserslautern-Landau University, Germany"}
  - {name: Nora Harrach, affiliation: "Eötvös Loránd University, Hungary"}
  - {name: Óscar Fernández Ayala, affiliation: "TU Braunschweig, Germany"}
  - {name: Rhys Evans, affiliation: "IMFM, Slovenia"}
  - {name: Russ Woodroofe, affiliation: "University of Primorska, Slovenia"}
  - {name: Sarah Rees, affiliation: "University of Newcastle, U.K."}
  - {name: Thomas Breuer, affiliation: "RWTH Aachen University, Germany"}
  - {name: Timo Velten, affiliation: "TU Braunschweig, Germany"}
  - {name: Vinay Wagh, affiliation: "IIT Guwahati, India"}
  - {name: Wilf Wilson}
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

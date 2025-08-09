---
layout: page
title: Participants
participants:
  - {name: Andoni Zozaya, affiliation: "Public University of Navarra, Spain"}
  - {name: Anton Betten, affiliation: "Kuwait University, Kuwait"}
  - {name: Antonio Montero, affiliation: "University of Ljubljana, Slovenia"}
  - {name: Bettina Eick, affiliation: "TU Braunschweig, Germany"}
  - {name: Bojan Kuzma, affiliation: "University of Primorska, Slovenia"}
  - {name: Charles Leedham-Green (online), affiliation: "Queen Mary University of London, U.K."}
  - {name: Cheryl Praeger (online), affiliation: "University of Western Australia, Australia"}
  - {name: Frank Lübeck, affiliation: "RWTH Aachen University, Germany"}
  - {name: George Savvoudis, affiliation: "University of Primorska, Slovenia"}
  - {name: Giusy Monzillo, affiliation: "University of Primorska, Slovenia"}
  - {name: Henrik Schanze, affiliation: "TU Braunschweig, Germany"}
  - {name: Innocent Opara, affiliation: "Institute of Mathematics, Nigeria"}
  - {name: István Szöllősi, affiliation: "Babeș-Bolyai University, Romania"}
  - {name: James Mitchell, affiliation: "University of St Andrews, U.K."}
  - {name: Jan De Beule, affiliation: "Vrije Universiteit Brussel, Belgium"}
  - {name: Joseph Edwards, affiliation: "University of St Andrews, U.K."}
  - {name: Leonard Soicher, affiliation: "Queen Mary University of London, U.K."}
  - {name: Leyla Işık, affiliation: "University of Primorska, Slovenia"}
  - {name: Lukas Schnelle, affiliation: "RWTH Aachen University, Germany"}
  - {name: Max Horn, affiliation: "RPTU Kaiserslautern-Landau University, Germany"}
  - {name: Meike Weiß, affiliation: "RWTH Aachen University, Germany"}
  - {name: Michel Lavrauw, affiliation: "University of Primorska, Slovenia"}
  - {name: Mike Ogiugo, affiliation: "Yaba College of Technology, Nigeria"}
  - {name: Milad Ahanjideh, affiliation: "University of Primorska, Slovenia"}
  - {name: Morgan Rodgers, affiliation: "RPTU Kaiserslautern-Landau University, Germany"}
  - {name: Neda Ahanjideh, affiliation: "Shahrekord University, Iran"}
  - {name: Nora Harrach, affiliation: "Eötvös Loránd University, Hungary"}
  - {name: Olexandr Konovalov, affiliation: "University of St Andrews, U.K."}
  - {name: Óscar Fernández Ayala, affiliation: "TU Braunschweig, Germany"}
  - {name: Rhys Evans, affiliation: "IMFM, Slovenia"}
  - {name: Russ Woodroofe, affiliation: "University of Primorska, Slovenia"}
  - {name: Sarah Rees, affiliation: "University of Newcastle, U.K."}
  - {name: Seyyed Ali Mohammadiyeh, affiliation: "Department of Pure Mathematics, Faculty of Mathematical Sciences, University of Kashan, Kashan 87317-53153, I. R. Iran"}
  - {name: Thomas Breuer, affiliation: "RWTH Aachen University, Germany"}
  - {name: Timo Velten, affiliation: "TU Braunschweig, Germany"}
  - {name: Vinay Wagh, affiliation: "IIT Guwahati, India"}
  - {name: Volkmar Welker, affiliation: "Philipps-Universität Marburg, Germany"}
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

---
layout: page
title: Participants
participants:
  - {name: "Andoni Zozaya", affiliation: "Public University of Navarra", country: "Spain", country_emoji: "🇪🇸", online: false}
  - {name: "Andrea Švob", affiliation: "University of Rijeka", country: "Croatia", country_emoji: "🇭🇷", online: false}
  - {name: "Anton Betten", affiliation: "Kuwait University", country: "Kuwait", country_emoji: "🇰🇼", online: false}
  - {name: "Antonio Montero", affiliation: "University of Ljubljana", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: "Bettina Eick", affiliation: "TU Braunschweig", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: "Bojan Kuzma", affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: "Charles Leedham-Green", affiliation: "Queen Mary University of London", country: "United Kingdom", country_emoji: "🇬🇧", online: true}
  - {name: "Cheryl Praeger", affiliation: "University of Western Australia", country: "Australia", country_emoji: "🇦🇺", online: true}
  - {name: "Dean Crnković", affiliation: "University of Rijeka", country: "Croatia", country_emoji: "🇭🇷", online: false}
  - {name: "Frank Lübeck", affiliation: "RWTH Aachen University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: "George Savvoudis", affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: "Giusy Monzillo", affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: "Henrik Schanze", affiliation: "TU Braunschweig", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: "Innocent Opara", affiliation: "Institute of Mathematics", country: "Nigeria", country_emoji: "🇳🇬", online: false}
  - {name: "István Szöllősi", affiliation: "Babeș-Bolyai University", country: "Romania", country_emoji: "🇷🇴", online: false}
  - {name: "James Mitchell", affiliation: "University of St Andrews", country: "United Kingdom", country_emoji: "🇬🇧", online: false}
  - {name: "Jan De Beule", affiliation: "Vrije Universiteit Brussel", country: "Belgium", country_emoji: "🇧🇪", online: false}
  - {name: "Joseph Edwards", affiliation: "University of St Andrews", country: "United Kingdom", country_emoji: "🇬🇧", online: false}
  - {name: "Leonard Soicher", affiliation: "Queen Mary University of London", country: "United Kingdom", country_emoji: "🇬🇧", online: false}
  - {name: "Leyla Işık", affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: "Lukas Schnelle", affiliation: "RWTH Aachen University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: "Max Horn", affiliation: "RPTU Kaiserslautern-Landau University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: "Meike Weiß", affiliation: "RWTH Aachen University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: "Michel Lavrauw", affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: "Mike Ogiugo", affiliation: "Yaba College of Technology", country: "Nigeria", country_emoji: "🇳🇬", online: false}
  - {name: "Milad Ahanjideh", affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: "Morgan Rodgers", affiliation: "RPTU Kaiserslautern-Landau University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: "Neda Ahanjideh", affiliation: "Shahrekord University", country: "Iran", country_emoji: "🇮🇷", online: false}
  - {name: "Nora Harrach", affiliation: "Eötvös Loránd University", country: "Hungary", country_emoji: "🇭🇺", online: false}
  - {name: "Olexandr Konovalov", affiliation: "University of St Andrews", country: "United Kingdom", country_emoji: "🇬🇧", online: false}
  - {name: "Óscar Fernández Ayala", affiliation: "TU Braunschweig", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: "Rhys Evans", affiliation: "IMFM", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: "Russ Woodroofe", affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: "Sarah Rees", affiliation: "University of Newcastle", country: "United Kingdom", country_emoji: "🇬🇧", online: false}
  - {name: "Seyyed Ali Mohammadiyeh", affiliation: "Department of Pure Mathematics, Faculty of Mathematical Sciences, University of Kashan", country: "Iran", country_emoji: "🇮🇷", online: false}
  - {name: "Thomas Breuer", affiliation: "RWTH Aachen University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: "Timo Velten", affiliation: "TU Braunschweig", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: "Vinay Wagh", affiliation: "IIT Guwahati", country: "India", country_emoji: "🇮🇳", online: false}
  - {name: "Volkmar Welker", affiliation: "Philipps-Universität Marburg", country: "Germany", country_emoji: "🇩🇪", online: false}
---

<ol>
{% for p in page.participants %}
  <li>
    <strong>{{ p.name }}</strong>
    {% if p.affiliation %} ({{ p.affiliation }}){% endif %}
    {% if p.country_emoji %} {{ p.country_emoji }}{% endif %}
    {% if p.online %}
      <span style="color: green;">[Online]</span>
    {% endif %}
    {% if p.links %}
      {% for item in p.links %}
        <a href="{{ item[1] }}">({{ item[0] }})</a>
      {% endfor %}
    {% endif %}
    <br/>
    {% if p.talk %} Talk: {{ p.talk }}{% endif %}
  </li>
{% endfor %}
</ol>

<h2>Participants by Country ({{ page.participants | size }})</h2>
<ul>
  {% assign grouped = page.participants | group_by: "country" %}

  {% assign country_counts = "" | split: "" %}

  {% for g in grouped %}
    {% assign count = g.items | size %}
    {% capture padded_count %}{% if count < 10 %}0{% endif %}{{ count }}{% endcapture %}
    {% capture entry %}{{ padded_count }}||{{ g.items[0].country_emoji }}||{{ g.name }}{% endcapture %}
    {% assign country_counts = country_counts | push: entry %}
  {% endfor %}

  {%- comment -%} Sort numerically descending by padded count {%- endcomment -%}
  {% assign sorted = country_counts | sort_natural | reverse %}

  {% for entry in sorted %}
    {% assign parts = entry | split: "||" %}
    {% assign count_num = parts[0] | plus: 0 %}
    <li>{{ parts[1] }} {{ parts[2] }}: {{ count_num }} participant{% if count_num > 1 %}s{% endif %}</li>
  {% endfor %}
</ul>

{% if site.data.feedback.size > 0 %}
<h2>Feedback</h2>
<ul>
{% for f in site.data.feedback %}
  <li>
    <strong>{{ f.name }}</strong>
    {% if f.package %} (author of {{ f.package }}){% endif %}
    <br/>
    {{ f.feedback }}
  </li>
{% endfor %}
</ul>
{% endif %}

<!--
<h2>Conference photo</h2>
<figure>
  <a href="{{ site.baseurl }}/public/conf_photo.jpg">
    <img 
      src="{{ site.baseurl }}/public/conf_photo.jpg" 
      alt="Group photo of GAP Days Summer 2025 participants at University of Primorska, Koper, Slovenia, 25-29 August 2025" 
      style="max-width:100%; height:auto;"
    />
  </a>
  <figcaption>
    GAP Days Summer 2025<br/>
    25-29 August 2025<br/>
    University of Primorska, Koper, Slovenia
  </figcaption>
</figure>
-->

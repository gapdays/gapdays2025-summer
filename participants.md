---
layout: page
title: Participants
participants:
  - {name: Andoni Zozaya, affiliation: "Public University of Navarra", country: "Spain", country_emoji: "🇪🇸", online: false}
  - {name: Andrea Švob, affiliation: "University of Rijeka", country: "Croatia", country_emoji: "🇭🇷", online: false}
  - {name: Anton Betten, affiliation: "Kuwait University", country: "Kuwait", country_emoji: "🇰🇼", online: false}
  - {name: Antonio Montero, affiliation: "University of Ljubljana", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: Bettina Eick, affiliation: "TU Braunschweig", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: Bojan Kuzma, affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: Charles Leedham-Green, affiliation: "Queen Mary University of London", country: "United Kingdom", country_emoji: "🇬🇧", online: true}
  - {name: Cheryl Praeger, affiliation: "University of Western Australia", country: "Australia", country_emoji: "🇦🇺", online: true}
  - {name: Dean Crnković, affiliation: "University of Rijeka", country: "Croatia", country_emoji: "🇭🇷", online: false}
  - {name: Frank Lübeck, affiliation: "RWTH Aachen University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: George Savvoudis, affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: Giusy Monzillo, affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: Henrik Schanze, affiliation: "TU Braunschweig", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: Innocent Opara, affiliation: "Institute of Mathematics", country: "Nigeria", country_emoji: "🇳🇬", online: false}
  - {name: István Szöllősi, affiliation: "Babeș-Bolyai University", country: "Romania", country_emoji: "🇷🇴", online: false}
  - {name: James Mitchell, affiliation: "University of St Andrews", country: "United Kingdom", country_emoji: "🇬🇧", online: false}
  - {name: Jan De Beule, affiliation: "Vrije Universiteit Brussel", country: "Belgium", country_emoji: "🇧🇪", online: false}
  - {name: Joseph Edwards, affiliation: "University of St Andrews", country: "United Kingdom", country_emoji: "🇬🇧", online: false}
  - {name: Leonard Soicher, affiliation: "Queen Mary University of London", country: "United Kingdom", country_emoji: "🇬🇧", online: false}
  - {name: Leyla Işık, affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: Lukas Schnelle, affiliation: "RWTH Aachen University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: Max Horn, affiliation: "RPTU Kaiserslautern-Landau University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: Meike Weiß, affiliation: "RWTH Aachen University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: Michel Lavrauw, affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: Mike Ogiugo, affiliation: "Yaba College of Technology", country: "Nigeria", country_emoji: "🇳🇬", online: false}
  - {name: Milad Ahanjideh, affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: Morgan Rodgers, affiliation: "RPTU Kaiserslautern-Landau University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: Neda Ahanjideh, affiliation: "Shahrekord University", country: "Iran", country_emoji: "🇮🇷", online: false}
  - {name: Nora Harrach, affiliation: "Eötvös Loránd University", country: "Hungary", country_emoji: "🇭🇺", online: false}
  - {name: Olexandr Konovalov, affiliation: "University of St Andrews", country: "United Kingdom", country_emoji: "🇬🇧", online: false}
  - {name: Óscar Fernández Ayala, affiliation: "TU Braunschweig", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: Rhys Evans, affiliation: "IMFM", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: Russ Woodroofe, affiliation: "University of Primorska", country: "Slovenia", country_emoji: "🇸🇮", online: false}
  - {name: Sarah Rees, affiliation: "University of Newcastle", country: "United Kingdom", country_emoji: "🇬🇧", online: false}
  - {name: Seyyed Ali Mohammadiyeh, affiliation: "Department of Pure Mathematics, Faculty of Mathematical Sciences, University of Kashan", country: "Iran", country_emoji: "🇮🇷", online: false}
  - {name: Thomas Breuer, affiliation: "RWTH Aachen University", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: Timo Velten, affiliation: "TU Braunschweig", country: "Germany", country_emoji: "🇩🇪", online: false}
  - {name: Vinay Wagh, affiliation: "IIT Guwahati", country: "India", country_emoji: "🇮🇳", online: false}
  - {name: Volkmar Welker, affiliation: "Philipps-Universität Marburg", country: "Germany", country_emoji: "🇩🇪", online: false}
---

<ol>
{% assign participants = page.participants %}
{% for p in participants %}
  <li>
    <strong>{{ p.name }}</strong>
    {% if p.affiliation != null %} ({{ p.affiliation }}){% endif %}
    {% if p.country_emoji != null %} {{ p.country_emoji }}{% endif %}
    {% if p.online %}
      <span style="color: green;">[Online]</span>
    {% endif %}
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

<h2>
  Participants by Country
  ({% assign total = 0 %}{% for p in page.participants %}{% assign total = total | plus: 1 %}{% endfor %}{{ total }})
</h2>
<ul>
{% assign grouped = page.participants | group_by: "country" %}

{%- assign max_count = 0 -%}
{%- for g in grouped -%}
  {%- assign c = g.items | size -%}
  {%- if c > max_count -%}{%- assign max_count = c -%}{%- endif -%}
{%- endfor -%}
{%- capture max_str -%}{{ max_count }}{%- endcapture -%}
{%- assign width = max_str | size -%}

{%- assign flat = "" | split: "" -%}
{%- for g in grouped -%}
  {%- assign c = g.items | size -%}
  {%- capture c_str -%}{{ c }}{%- endcapture -%}
  {%- assign c_len = c_str | size -%}
  {%- assign zeros_to_add = width | minus: c_len -%}
  {%- if zeros_to_add > 0 -%}
    {%- capture zeros -%}{% for i in (1..zeros_to_add) %}0{% endfor %}{%- endcapture -%}
  {%- else -%}
    {%- assign zeros = "" -%}
  {%- endif -%}
  {%- assign padded = zeros | append: c_str -%}
  {%- assign entry = padded | append: "||" | append: g.items[0].country_emoji | append: "||" | append: g.name | append: "||" | append: c_str -%}
  {%- assign flat = flat | push: entry -%}
{%- endfor -%}

{%- assign sorted = flat | sort | reverse -%}

{% for entry in sorted %}
  {%- assign parts = entry | split: "||" -%}
  {%- assign emoji = parts[1] -%}
  {%- assign name = parts[2] -%}
  {%- assign count = parts[3] -%}
  <li>{{ emoji }} {{ name }}: {{ count }} participant{% if count | plus: 0 > 1 %}s{% endif %}</li>
{% endfor %}
</ul>

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

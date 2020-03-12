---
layout: page
title: O podcaście
---

Trójka przyjaciół rozmawia o tematach technologicznych. Na niektórych tematach się znamy, a na niektórych nie. Używamy prostego języka, aby słuchanie było przyjemnością. Dokładamy jednak starań, żeby nasze wywody były spójne i poprawne logicznie. Życzymy miłego słuchania!

## [](#header-2)Zespół

*   Damian. Bloguje na [jakbadacdane.pl](https://jakbadacdane.pl/). Odcinki w których można go usłyszeć: {% site.tags.damian %}
*   Gosia. Trenuje tancerzy w [Irish Spin](https://taniec-irlandzki.wroclaw.pl/). Odcinki w których można ją usłyszeć: 
*   Karol. Tajemniczy niczym [Stig](https://pl.wikipedia.org/wiki/Stig). Odcinki w których można go usłyszeć: 


<ul class="tags">
{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}
  <li>{{t | downcase | replace:" ","-" }} has {{ posts | size }} posts</li>
{% endfor %}
</ul>



{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

{{ t | downcase }}
<ul>
{% for post in posts %}
  {% if post.tags contains t %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="date">{{ post.date | date: "%B %-d, %Y"  }}</span>
  </li>
  {% endif %}
{% endfor %}
</ul>
{% endfor %}
---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

{% for election in site.elections %}
  <h2>
    <a href="{{ election.url }}">
      {{ election.date | date: "%d/%m" }} - {{ election.country }} - {{ election.title }}
    </a>
  </h2>
  <p>{{ election.content | markdownify }}</p>
{% endfor %}
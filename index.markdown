---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---


<style type="text/css">
  .election {
    border: 1px solid black;
    border-width: 0px 0px 0px 1px ;
    margin: 10px 0px 10px 0px;
    padding: 0px 0px 0px 10px;
  }
</style>

{% for election in site.elections %}
<article class="election">
  <h1>{{ election.date | date_to_long_string }}</h1>
  <h2>{{ election.title }}</h2>
  <a href="{{ election.url }}"> Ver mas</a>
</article>
{% endfor %}

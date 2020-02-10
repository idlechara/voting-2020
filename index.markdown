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

<h1>Lista de elecciones confirmadas:</h1>

<p>A continuación se presenta una lista de los procesos electorales para el año 2020 que hayan sido validados por las instituciones/organizaciones que las efectúan:</p>

{% for election in site.elections %}
<article class="election">


  {% assign months = "Enero|Febrero|Marzo|Abril|Mayo|Junio|Julio|Agosto|Septiembre|Octubre|Noviembre|Diciembre" | split: "|" %}
  {% assign m = election.date | date: "%-m" | minus: 1 %}
  {% assign day = election.date | date: "%d" %}
  {% assign month = months[m] %}
  {% assign year = election.date | date: "%Y" %}

  <h2>{{ day }} de {{ month }}</h2>
  <h3>{{ election.title }}</h3>
  <a href="{{ election.url  | prepend: site.baseurl }}"> Ver mas</a>
</article>
{% endfor %}

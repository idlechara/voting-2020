---
layout: default
---

<article class="post h-entry" itemscope itemtype="http://schema.org/BlogPosting">

  <header class="post-header">
    <h1 class="post-title p-name" itemprop="name headline">{{ page.title | escape }}</h1>
    <p class="post-meta">

    {% assign months = "Enero|Febrero|Marzo|Abril|Mayo|Junio|Julio|Agosto|Septiembre|Octubre|Noviembre|Diciembre" | split: "|" %}
    {% assign m = page.date | date: "%-m" | minus: 1 %}
    {% assign day = page.date | date: "%d" %}
    {% assign month = months[m] %}
    {% assign year = page.date | date: "%Y" %}

    <time class="dt-published" datetime="{{ page.date | date_to_xmlschema }}" itemprop="datePublished">
    {{ day }} de {{ month }} de {{year}}
    </time>
    
    {%- if page.author -%}
    • {% for author in page.author %}
        <span itemprop="author" itemscope itemtype="http://schema.org/Person">
        <span class="p-author h-card" itemprop="name">{{ author }}</span></span>
        {%- if forloop.last == false %}, {% endif -%}
    {% endfor %}
    {%- endif -%}</p>
  </header>

  <div class="post-content e-content" itemprop="articleBody">

    <a href={{page.wikipedia}} > Wikipedia </a>
    <br>
    <a href={{page.official_site}} > Sitio Oficial </a>

    {{ content }}
  </div>

  {%- if site.disqus.shortname -%}
    {%- include disqus_comments.html -%}
  {%- endif -%}

  <a class="u-url" href="{{ page.url | relative_url }}" hidden></a>
</article>

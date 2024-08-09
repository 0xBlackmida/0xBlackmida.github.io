---
layout: default
category: tech
---

<h1>Articoli nella categoria: {{ page.category | capitalize }}</h1>

<ul>
  {%- for post in site.posts -%}
    {%- if post.categories contains page.category -%}
      <li>
          [ {{ post.date | date: "%d-%m-%Y" }} ] <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
          <p></p>
      </li>
    {%- endif -%}
  {%- endfor -%}
</ul>
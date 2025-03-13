---
layout: page
title: CATEGORIE
permalink: /lab
---

# SOME EXP.

<!-- INIZIO MENU CATEGORIE -->

{%- assign unique_categories = "" | split: "" -%}
{%- for post in site.posts -%}
  {%- for category in post.categories -%}
    {%- unless unique_categories contains category -%}
      {%- assign unique_categories = unique_categories | push: category -%}
    {%- endunless -%}
  {%- endfor -%}
{%- endfor -%}

<center>
  {%- if unique_categories.size > 0 -%}
    {%- for category in unique_categories -%}
      {%- if forloop.first == false -%} | {%- endif -%}
      <a href="{{ site.baseurl }}/{{ category | downcase | replace: ' ', '-' }}" style="text-decoration: none !important;">
         🏷️{{ category }} 
      </a>
    {%- endfor -%}
  {%- endif -%}
</center>


<!-- FINE MENU CATEGORIE -->
---
layout: base
title: Markus was here
pagination:
  data: collections.general
  size: 2
  alias: posts
---
My first test, this is amazing.


## My posts 1

{%- for post in collections.general %}
- [{{ post.data.title }}]({{ post.url }})
{%- endfor %}
## My posts 2

{%- for post in posts %}
- [{{ post.data.title }}]({{ post.url }})
{%- endfor %}

{% if pagination.href.previous %}
  <a href="{{pagination.href.previous}}">Previous Page</a>
{% endif %}
{% if pagination.href.next %}
  <a href="{{pagination.href.next}}">Next Page</a>
{% endif %}
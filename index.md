---
layout: page
title: Tim Slatcher
tagline: is a second year Computer Science student at Oxford University
---
{% include JB/setup %}

{% for post in site.posts %}
    {% if forloop.first %}

<h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a> <small>{{ post.tagline }}</small></h2>


<div class="row">
  <div class="span8">
    {{ post.content }}
  </div>
</div>
  
<div class="pagination">
  <ul>
  {% if post.previous %}
    <li class="prev"><a href="{{ BASE_PATH }}{{ post.previous.url }}" title="{{ post.previous.title }}">&larr; Previous</a></li>
  {% else %}
    <li class="prev disabled"><a>&larr; Previous</a></li>
  {% endif %}
<li><a href="{{ BASE_PATH }}{{ site.JB.archive_path }}">Archive</a></li>
  {% if post.next %}
    <li class="next"><a href="{{ BASE_PATH }}{{ post.next.url }}" title="{{ post.next.title }}">Next &rarr;</a></li>
  {% else %}
    <li class="next disabled"><a>Next &rarr;</a></li>
  {% endif %}
    </ul>
</div>
    {% endif %}

  {% endfor %}
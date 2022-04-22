---
layout: page
title: Blog Archive
---
<img src="http://fckstudentloans.com/assets/img/bg-masthead.jpg" style="width: 100%; height: 100px; object-fit: cover;object-position: 0 45%" />

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.date | date: "%B %Y" }} - {{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

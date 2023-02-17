---
layout: page
image:  /assets/banner.jpg
---

Probably not worth reading.

<html>
{% assign postsByYear = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
    {% for year in postsByYear %}
      <h1>{{ year.name }}</h1>
      {% assign postsByMonth = year.items | group_by_exp:"post", "post.date | date: '%B'" %}

      {% for month in postsByMonth %}
        <h2>{{ month.name }}</h2>
        <ul>
          {% for post in month.items %}
            <li><a href="{{ post.url }}">{{ post.title }} - {{ post.date | date: '%A %e %B' }}</a></li>
          {% endfor %}
        </ul>

      {% endfor %}
    {% endfor %}
</html>

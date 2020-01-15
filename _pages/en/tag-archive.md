---
title: "People working on research fields"
layout: archive
permalink: /tags/
---


![Keywords ERPI](/assets/images/about/Keywords-ERPI.png)

{% assign entries = site.people | where: "lang", page.lang %}

{% include group-by-array.html collection=entries field='tags' %}

<ul class="taxonomy__index">
  {% for tag in group_names %}
    {% assign posts = group_items[forloop.index0] %}

    <li>
      <h2>{{ tag }}</h2>
      <ul>
        {% for post in posts %}
        <li>
          <a href='{{ site.baseurl }}{{ post.url }}'>{{ post.title }}</a>
        </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>


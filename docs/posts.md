---
title: Posts
permalink: /posts/
---


# Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

## Posts by tag


{% for tag in site.tags %}
  ### {{ tag[0] }}
  <ul>
    {{% for post in tag[1] %}}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
{{% endfor %}}
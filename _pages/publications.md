---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

<style>
.pub-list {
  list-style: none;
  padding: 0;
}
.pub-item {
  margin-bottom: 1.5em;
  padding-bottom: 1em;
  border-bottom: 1px solid #eee;
}
.pub-title {
  font-size: 1.1em;
  font-weight: 600;
  margin-bottom: 0.3em;
}
.pub-title a {
  color: #494e52;
  text-decoration: none;
}
.pub-title a:hover {
  color: #0066cc;
  text-decoration: underline;
}
.pub-authors {
  color: #666;
  margin-bottom: 0.2em;
}
.pub-venue {
  font-style: italic;
  color: #888;
  font-size: 0.95em;
}
</style>

<ul class="pub-list">
{% for post in site.publications reversed %}
  <li class="pub-item">
    <div class="pub-title">
      {% if post.paperurl %}
        <a href="{{ post.paperurl }}">{{ post.title }}</a>
      {% else %}
        {{ post.title }}
      {% endif %}
    </div>
    {% if post.authors %}
      <div class="pub-authors">
        {{ post.authors | replace: "Kuei-Hsiang Huang", "<strong>Kuei-Hsiang Huang</strong>" }}
      </div>
    {% endif %}
    {% if post.venue %}
      <div class="pub-venue">{{ post.venue }}{% if post.date %}, {{ post.date | date: "%Y" }}{% endif %}</div>
    {% endif %}
  </li>
{% endfor %}
</ul>
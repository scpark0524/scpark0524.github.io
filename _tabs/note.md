---
layout: page
title: Note
icon: fas fa-pen-nib
order: 2
---

<style>
.note-card {
  background: rgba(255,255,255,.03);
  border: 1px solid rgba(255,255,255,.06);
  border-radius: 14px;
  padding: 1.5rem;
  margin-bottom: 1rem;
  transition: all .3s ease;
}
.note-card:hover {
  border-color: rgba(74, 158, 255, .15);
  background: rgba(255,255,255,.06);
  transform: translateY(-2px);
}
.note-card a.note-title {
  font-size: 1.15rem;
  font-weight: 700;
  color: #e6edf3;
  text-decoration: none;
  display: block;
  margin-bottom: .4rem;
}
.note-card a.note-title:hover {
  color: #4a9eff;
}
.note-date {
  font-size: .78rem;
  color: #6e7681;
  margin-bottom: .6rem;
}
.note-excerpt {
  font-size: .88rem;
  color: #8b949e;
  line-height: 1.65;
}
</style>

{% assign notes = site.categories['Note'] %}
{% if notes.size > 0 %}
{% for post in notes %}
<div class="note-card">
  <a href="{{ post.url }}" class="note-title">{{ post.title }}</a>
  <div class="note-date">{{ post.date | date: "%Y.%m.%d" }}</div>
  {% if post.excerpt %}
  <div class="note-excerpt">{{ post.excerpt | strip_html | truncate: 150 }}</div>
  {% endif %}
</div>
{% endfor %}
{% else %}
<p style="color: #8b949e;">아직 작성된 노트가 없습니다.</p>
{% endif %}

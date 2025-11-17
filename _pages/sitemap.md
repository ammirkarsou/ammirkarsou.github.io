---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

<style>
.sitemap-list {
  list-style: none;
  margin-left: 0;
  padding-left: 0;
}
.sitemap-list li {
  margin-bottom: 0.35rem;
}
.sitemap-meta {
  font-size: 0.85em;
  color: var(--global-text-color-light);
  margin-left: 0.35rem;
}
</style>

<p>This human-friendly sitemap highlights every major section of the site. If you prefer machine-readable lists, grab the <a href="{{ base_path }}/sitemap.xml">XML sitemap</a>.</p>

{% assign nav_items = site.data.navigation.main %}

<h2>Main navigation</h2>
<ul class="sitemap-list">
  {% for item in nav_items %}
    {% if item.url %}
    <li><a href="{{ item.url | prepend: base_path }}">{{ item.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

{% assign publications = site.publications | sort: "date" | reverse %}
<h2>Publications</h2>
{% if publications and publications.size > 0 %}
<ul class="sitemap-list">
  {% for post in publications %}
    <li><a href="{{ post.url | prepend: base_path }}">{{ post.title }}</a> <span class="sitemap-meta">{{ post.date | date: "%b %Y" }}</span></li>
  {% endfor %}
</ul>
{% else %}
<p>No publications published yet.</p>
{% endif %}

{% assign posts = site.posts | sort: "date" | reverse %}
<h2>Blog posts</h2>
{% if posts and posts.size > 0 %}
<ul class="sitemap-list">
  {% for post in posts %}
    <li><a href="{{ post.url | prepend: base_path }}">{{ post.title }}</a> <span class="sitemap-meta">{{ post.date | date: "%b %Y" }}</span></li>
  {% endfor %}
</ul>
{% else %}
<p>Long-form articles are under construction—check back soon.</p>
{% endif %}

{% assign portfolio_items = site.portfolio | sort: "date" | reverse %}
<h2>Portfolio</h2>
{% if portfolio_items and portfolio_items.size > 0 %}
<ul class="sitemap-list">
  {% for item in portfolio_items %}
    <li><a href="{{ item.url | prepend: base_path }}">{{ item.title }}</a> <span class="sitemap-meta">{{ item.date | date: "%b %Y" }}</span></li>
  {% endfor %}
</ul>
{% else %}
<p>The portfolio showcase is being curated and will be published soon.</p>
{% endif %}

{% assign nav_urls = "" %}
{% for item in nav_items %}
  {% if item.url %}
    {% assign nav_urls = nav_urls | append: item.url | append: "|" %}
  {% endif %}
{% endfor %}

{% assign extra_pages = site.pages | sort: "title" %}
<h2>Additional pages</h2>
<ul class="sitemap-list">
{% for page in extra_pages %}
  {% if page.title and page.url and page.url != "/" and page.url != "/feed.xml" and page.sitemap_exclude != true %}
    {% unless nav_urls contains page.url %}
      <li><a href="{{ page.url | prepend: base_path }}">{{ page.title }}</a></li>
    {% endunless %}
  {% endif %}
{% endfor %}
</ul>

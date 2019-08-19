---
layout: archive
permalink: /blog-posts/
title: "Blog"
author_profile: true
---

{% if page.id and page.related and site.related_posts.size > 0 %}
  <div class="page___related">
    {% if site.data.ui-text[site.locale].related_label %}
      <h4 class="page__related-title">{{ site.data.ui-text[site.locale].related_label | default: "You May Also Enjoy" }}</h4>
    {% endif %}
    <div class="grid__wrapper">
      {% for post in site.related_posts limit:3 %}
        {% include archive-single.html type="grid" %}
      {% endfor %}
    </div>
  </div>
{% endif %}

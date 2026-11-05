---
layout: home
author_profile: true
---

{% assign featured_post = site.posts | where: "featured", true | first %}
{% if featured_post %}
<div class="page__hero--overlay" style="background-image: linear-gradient(rgba(0, 0, 0, 0.65), rgba(0, 0, 0, 0.65)), url('{{ featured_post.header.image | relative_url }}'); margin-bottom: 3em; border-radius: 8px; padding: 4em 2em;">
  <div class="wrapper" style="text-align: center;">
    <h2 class="page__title" style="color: white; margin-top: 0;">{{ featured_post.title }}</h2>
    <p class="page__lead" style="color: #e0e0e0; font-size: 1.1em; max-width: 800px; margin: 0 auto 1.5em auto;">
      {{ featured_post.excerpt | strip_html | truncatewords: 30 }}
    </p>
    <p><a href="{{ featured_post.url | relative_url }}" class="btn btn--light-outline btn--large">Read more</a></p>
  </div>
</div>
{% endif %}

## Recent Posts

---
layout: default
title: Home Page
---

<main class="feed">

  <section>
    <div id="bio">
      <div id="bio-avatar-wrapper">
        <img src="{{ site.data.author.avatar }}" alt="Avatar missing" id="bio-avatar" />
      </div>

      <div id="bio-text">{{ site.data.author.description }}</div>
    </div>

    <div id="social-links">
    {% for i in site.data.author.contact %}
      <a href="{{i.url}}" target="_blank">
        <i class="bi bi-{{i.title}}"></i>
      </a>
    {%endfor%}
    </div>
  </section>

  {% include _posts.html posts=site.posts %}

</main>
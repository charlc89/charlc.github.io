---
title: 
feature_text: |
  # Charles 
  The journey from a naïve person to a mature immunologist
  
feature_image: "https://i.pinimg.com/originals/3b/8a/d2/3b8ad2c7b1be2caf24321c852103598a.jpg"
excerpt: "But man is made for defeat. A man can be destroyed, but not defeated --Ernest Hemingway."
---

<main class="main  container">

  <div class="content">

    <article class="article  article--page  typeset">

      {% if paginator.posts %}
        {% assign collectiondata = site.collections | where: "label", page.collectionpage | first %}
        <h1>{{ collectiondata.title }}</h1>
        {{ collectiondata.description | markdownify }}

      {% else %}
        <h1>{{ page.title }}</h1>
        {{ content }}
        
      {% endif %}

    </article>

    {% include post-list.html %}

  </div>

  {% if page.aside == true %}{% include site-aside.html %}{% endif %}

</main>

---
layout: default
---

<header>
  <h1>{{ page.title }}</h1>
  <time>{{ page.date | date: "%B %d, %Y" }} – Written by {{ page.author }}</time>
</header>

<div id="post-container">
  <article>
    {{ content }}
  </article>
</div>
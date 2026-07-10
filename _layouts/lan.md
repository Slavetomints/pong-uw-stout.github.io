---
layout: default
---

<header>
  <h1>{{ page.title }}</h1>
  <time>{{ page.start_date | date: "%B %d, %Y" }} - {{ page.end_date | date :"%B %d, %Y" }}</time>
</header>

<div id="post-container">
  <article>
    {{ content }}
  </article>
</div>
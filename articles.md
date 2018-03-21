---
layout: default
permalink: /articles
---

## Articles

<section class="post-list">
  <div class="container">
   <ul>
    {% assign sorted = site.articles | sort: 'date' | reverse %}
    {% for post in sorted %}
    <li>
     <div class="ann">
      <span class="ann-title"><a href="/download/articles/{{ post.article }}">{{ post.title }}</a></span>
      <span class="ann-date">[{{ post.date | date: "%Y %b %d" }}]</span>
     </div>
    </li>
    {% endfor %}
   </ul>
  </div>
</section>

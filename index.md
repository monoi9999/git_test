---
layout: default
title: 모노의 블로그
---

<div class="home">
  <h1 class="page-heading">모노의 블로그</h1>
  <p>AI / 데이터 분석을 공부하면서 정리한 기록을 올리는 공간입니다.</p>

  <h2 class="post-list-heading">Posts</h2>
  <ul class="post-list">
    {%- assign sorted_posts = site.posts | sort: 'date' -%}
    {%- for post in sorted_posts -%}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
    </li>
    {%- endfor -%}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>
</div>

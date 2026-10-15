---
layout: page
title: Blog
permalink: /blog/
description: 공부하고 정리한 내용들을 모아둔 곳입니다.
nav: true
nav_order: 3
---

<!--
  이 목록은 자동으로 만들어집니다.
  _pages 폴더의 파일 중 앞부분(--- 사이)에 `blog: true` 가 있는 페이지가 여기에 나타납니다.
  순서는 `blog_order` 숫자가 작은 것부터입니다.
-->

{% assign blog_pages = site.pages | where: "blog", true | sort: "blog_order" %}

<ul class="blog-link-list">
  {% for item in blog_pages %}
    <li>
      <a href="{{ https://www.tistory.com/ }}"><strong>{{ item.title }}</strong></a>
      {% if item.description %}— {{ item.description }}{% endif %}
    </li>
  {% endfor %}
</ul>

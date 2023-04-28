---
layout: section
title: Tier2 Courses
summary: All the training opportunities available from UK Tier2 centres
banner: web_banners_02.jpg
---

<!--
Filter news by tags :  <a href="/about/news/blog"><code class="highligher-rouge"><nobr>blog</nobr></code>&nbsp;</a>        <a href="/about/news/calls"><code class="highligher-rouge"><nobr>calls</nobr></code>&nbsp;</a>        <a href="/about/news/events"><code class="highligher-rouge"><nobr>events</nobr></code>&nbsp;</a>        <a href="/about/news/newsletters"><code class="highligher-rouge"><nobr>newsletters</nobr></code>&nbsp;</a>     <!--   <a href="/about/news/"><code class="highligher-rouge"><nobr>show all</nobr></code>&nbsp;</a>   -->


<p>&nbsp;</p>


{% for course in site.courses %}
<div class="course-area">
  <a href="{{ course.url | prepend: site.baseurl }}" class="bold">{{ course.title }}</a> &nbsp; &nbsp; &nbsp;
  {{ course.tier2 }}

  <p class="course-date">

{{ course.start_date | date_to_string }} - {{ course.end_date | date_to_string }}

  &nbsp;&nbsp;&nbsp;&nbsp;
  {{ course.author }}

      &nbsp;&nbsp;&nbsp;&nbsp;
      {% for tag in course.tags %}
        {% capture tag_name %}{{ tag }}{% endcapture %}
        <a href="/about/news/{{ tag_name }}" ><code  style="font-size:15px;"><nobr>{{ tag_name }}</nobr></code>&nbsp;</a>
      {% endfor %}         
  </p>

  <p>
    {{ course.content | strip_html | truncatewords: 50 }}
  </p>

  <p>
    <hr/>
  </p>
</div>
{% endfor %}





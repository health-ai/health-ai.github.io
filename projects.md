---
layout: page
title: Projects
---
<h3>Projects</h3>
Many students look for projects for classes or for summer internship. Here we list projects from graduate students, postdocs and faculty that could turn into valuable scientific contribution.

{% for item in site.projects %}
  <hr />
  <h3 class="projects">{{ item.title }}</h3>
  <p>{{ item.content }}</p>
  <p>Keywords: {{ item.keywords }}</p>
  <p>Contact: {{ item.contact.name }} ({{ item.contact.email }})</p>
{% endfor %}

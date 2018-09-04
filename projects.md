---
title: Projects
layout: page
---

<h3>Projects</h3>
Many students look for projects for classes or for summer internship. Here we list projects from graduate students, postdocs and faculty that could turn into valuable scientific contribution.

If you are affiliated with Stanford (valid address @stanford.edu) and you want to add your project [please fill in this form](). As soon as your project is accepted it will appear here.

{% for item in site.projects %}
  <hr />
  <h3 class="projects">{{ item.title }}</h3>
  <p>{{ item.content }}</p>
  <p>Keywords: {{ item.keywords }}</p>
  <p>Contact: {{ item.contact.name }} ({{ item.contact.email }})</p>
{% endfor %}

---
layout: page
permalink: /inventory/index.html
title: Inventory
image:
  feature: interior_1.jpg
---

{% for subject_hash in site.data.inventory.subjects %}
{% assign subject = subject_hash[1] %}
*   {{ subject.name }} ({{ subject.books | size }} books)
{% endfor %}

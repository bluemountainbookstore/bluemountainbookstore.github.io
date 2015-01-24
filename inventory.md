---
layout: page
permalink: /inventory/index.html
title: Inventory
image:
  feature: interior_1.jpg
---

{% for subject_hash in site.data.inventory.subjects %}
{% assign subject = subject_hash[1] %}
* {{ subject.name}} ({{ subject.works | size }} titles)
{% for work_hash in subject.works %}
{% assign work = work_hash[1] %}
    * _{{ work.book.title }}_ by {{ work.book.author }}
{% endfor %}
{% endfor %}

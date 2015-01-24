---
layout: page
permalink: /inventory/index.html
title: Online Inventory
image:
  feature: interior_1.jpg
---

{% for subject_hash in site.data.inventory.subjects %}
{% assign subject = subject_hash[1] %}
* {{ subject.name}} ({{ subject.works.size | pluralize: "title" }})
{% for work_hash in subject.works %}
{% assign work = work_hash[1] %}
    * _{{ work.book.title }}_ by {{ work.book.author }} ({{ work.copies.size | pluralize: "copy", "copies" }})
{% endfor %}
{% endfor %}

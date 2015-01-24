---
layout: page
permalink: /inventory/index.html
title: Inventory
image:
  feature: interior_1.jpg
---

{% for subject_hash in site.data.inventory.subjects %}
{% assign subject = subject_hash[1] %}
* {{ subject_hash[0] }} ({{ subject.books | size }} books)
{% for book_hash in subject.books %}
{% assign book = book_hash[1] %}
    * _{{ book.title }}_ by {{ book.author }}
{% endfor %}
{% endfor %}

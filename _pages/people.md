---
title: "People"
permalink: /people/
description: "The members and officers of the Clemson Amateur Radio Club (WD4EOG), and how to reach us."
---

{% assign people = site.data.people %}
{%- if people.group_photo and people.group_photo != "" %}
<figure class="group-photo">
<img src="{{ people.group_photo | relative_url }}" alt="{{ people.group_caption | default: 'Club members' | escape }}">
{%- if people.group_caption and people.group_caption != "" %}<figcaption>{{ people.group_caption }}</figcaption>{% endif %}
</figure>
{%- endif %}

## Officers

{% include club/officers.html %}

## Contact

{% include club/contact.html %}

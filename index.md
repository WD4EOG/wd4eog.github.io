---
layout: splash
title: "Clemson Amateur Radio Club"
excerpt: "Amateur radio practice, education and public service at Clemson since 1946."
header:
  overlay_image: /assets/img/towers.jpg
  overlay_filter: rgba(46, 26, 71, 0.7) # dark purple tint over the photo
  actions:
    - label: "Come to a meeting"
      url: /calendar/
feature_row:
  - title: "Dashboards"
    excerpt: "Live station and system data, plus band conditions."
    url: /dashboards/
    btn_label: "View dashboards"
    btn_class: "btn--primary"
  - title: "Calendar & meetups"
    excerpt: "Nets, meetings and events."
    url: /calendar/
    btn_label: "See the calendar"
    btn_class: "btn--primary"
  - title: "Repeaters"
    excerpt: "Frequencies, offsets and tones."
    url: /repeaters/
    btn_label: "Repeater info"
    btn_class: "btn--primary"
  - title: "Resources"
    excerpt: "Get licensed, learn Morse code and listen in."
    url: /resources/
    btn_label: "Start learning"
    btn_class: "btn--primary"
  - title: "About the club"
    excerpt: "Who we are and how to join."
    url: /about/
    btn_label: "About us"
    btn_class: "btn--primary"
---

## Next on the schedule

{% include club/meetups.html limit=1 %}

## Explore

{% include feature_row %}

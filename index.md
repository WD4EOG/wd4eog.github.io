---
layout: splash
title: "Clemson Amateur Radio Club"
excerpt: "Amateur radio practice, education and public service at Clemson since 1946."
header:
  overlay_image: /assets/img/towers.jpg
  overlay_filter: rgba(46, 26, 71, 0.7) # dark purple tint over the photo
  actions:
    - label: "Come to a meeting"
      url: /about/#get-involved
feature_row:
  - title: "About the club"
    excerpt: "Who we are, when we meet, and how to get licensed."
    url: /about/
    btn_label: "About us"
    btn_class: "btn--primary"
  - title: "Blog"
    excerpt: "Updates on our projects and activities."
    url: /blog/
    btn_label: "Read the blog"
    btn_class: "btn--primary"
  - title: "The shack"
    excerpt: "Our station, repeaters, live data and how-to guides."
    url: /shack/
    btn_label: "Tour the shack"
    btn_class: "btn--primary"
  - title: "People"
    excerpt: "Meet the officers and get in touch."
    url: /people/
    btn_label: "Meet us"
    btn_class: "btn--primary"
---

## Next on the schedule

{% include club/meetups.html limit=1 %}

## Latest from the blog

{% include club/recent-posts.html limit=3 %}

## Explore

{% include feature_row %}

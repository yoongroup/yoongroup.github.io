---
title: Team
nav:
  order: 3
  tooltip:
---

# {% include icon.html icon="fa-solid fa-users" %}Team

{% include section.html %}

## Current Members

{% include list.html  data="members"  component="portrait"  filters="role: pi" %}
{% include list.html  data="members"  component="portrait"  filters="role: current-postdoc" %}
{% include list.html  data="members"  component="portrait"  filters="role: current-phd" %}
{% include list.html  data="members"  component="portrait"  filters="role: current-undergrad" %}

{% include section.html %}

## Alumni

{% include list.html data="members" component="portrait" filters="role: postdoc-alum" %}
{% include list.html data="members" component="portrait" filters="role: phd-alum" %}
{% include list.html data="members" component="portrait" filters="role: ms-alum" %}
{% include list.html data="members" component="portrait" filters="role: undergrad-alum" %}

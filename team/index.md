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
{% include list.html  data="members"  component="portrait"  filters="role: current-innocore-postdoc" %}
{% include list.html  data="members"  component="portrait"  filters="role: current-phd" %}
{% include list.html  data="members"  component="portrait"  filters="role: current-grad" %}
{% include list.html  data="members"  component="portrait"  filters="role: current-undergrad" %}
{% include list.html  data="members"  component="portrait"  filters="role: current-intern" %} 

{% include section.html %}

## Alumni

{% comment %}
Original role-based alumni lists retained for reference:

{% include list.html data="members" component="portrait" filters="role: alum-postdoc" %}
{% include list.html data="members" component="portrait" filters="role: alum-phd" %}
{% include list.html data="members" component="portrait" filters="role: alum-ms" %}
{% include list.html data="members" component="portrait" filters="role: alum-undergrad" %}
{% endcomment %}

{% assign alumni = site.members
  | where_exp: "member", "member.role contains 'alum-'"
  | sort: "departure_date"
  | reverse
%}

{% for member in alumni %}
  {% include portrait.html lookup=member.slug %}
{% endfor %}

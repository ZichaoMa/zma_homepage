---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

**Two-dimensional material transistor technology and device physics**

Development of channel-integrated, high-mobility complementary transistor technology using two-dimensional (2D) semiconductors for 1 nm-node integrated circuits. First-principles calculations are used to model the device physics of 2D material to metal contacts, informing contact engineering, controllable doping methods, and stable van der Waals stacking processes toward 2D monolayer-body-channel gate-all-around (MBC-GAA) field-effect transistors. This work has yielded homogeneously integrated complementary logic circuits in MoS<sub>2</sub>, and complementary MoS<sub>2</sub> inverters built from fully 2D metal-insulator-semiconductor stacks incorporating h-BN and graphene.

**Nanostructured optoelectronic memristor design and on-chip integration**

Integration of photodetection and memristive switching into a single edge device for sensing-computing convergence, where nanostructuring further enables high-resolution imaging and high-density information processing. This research uses three-dimensional perovskite nanowire and quantum-wire arrays to fabricate optoelectronic memristors, applies first-principles molecular dynamics to model multi-level resistive switching, and develops CMOS-compatible integration methods for functional circuits.

<!--
TODO: add 2-3 figures here (device schematics, band diagrams, key results).
Put image files in /images/ and uncomment/adapt lines like:

<img src="{{ base_path }}/images/research-fig1.png" alt="Description of figure" style="max-width:100%; margin: 1em 0;">
<img src="{{ base_path }}/images/research-fig2.png" alt="Description of figure" style="max-width:100%; margin: 1em 0;">
-->

## Publications

{% assign pubs_sorted = site.publications | sort: "date" | reverse %}
{% assign pubs_by_year = pubs_sorted | group_by_exp: "pub", "pub.date | date: '%Y'" %}
{% for yeargroup in pubs_by_year %}
### {{ yeargroup.name }}

{% for pub in yeargroup.items %}
**{{ pub.title }}**

{{ pub.authors | replace: "Zichao Ma", "**Zichao Ma**" }}{% if pub.note != "" %}. *{{ pub.note }}*{% endif %}. {{ pub.venue }}{% if pub.details != "" %}, {{ pub.details }}{% endif %}, {{ pub.date | date: "%Y" }}.

{% endfor %}
{% endfor %}

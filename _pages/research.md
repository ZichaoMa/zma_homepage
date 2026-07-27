---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

**Two-dimensional material device technology and device physics**

*Dipole-induced p-type Ohmic contact in 2D FETs.* Doping the region of the two-dimensional (2D) semiconductor layer beneath the metal contact, whether through substitutional transition-metal atoms or chalcogen-site substitution, redistributes local charge and gives rise to an interface dipole. This dipole lowers the Schottky barrier in linear proportion to the doping concentration, establishing doping as a tractable engineering route to p-type Ohmic contact, long a missing capability in 2D FETs. The mechanism has been validated in Nb-doped MoS<sub>2</sub> and O-substituted WSe<sub>2</sub> FETs through combined first-principles simulation and experimental characterization. Beyond contact engineering, the group's broader interests span the atomistic molecular dynamics of nanostructured perovskites, photonics in 2D layered heterojunctions, and the homogeneous integration of complementary 2D FETs into inverter circuits.

<div style="display:flex; flex-wrap:wrap; gap:1.5em; margin: 1.5em 0;">
  <figure style="width:200px; margin:0;">
    <img src="{{ base_path }}/images/research-cover-nanoscale-2025.jpg" alt="Journal cover" style="width:100%; height:auto;">
  </figure>
  <figure style="width:200px; margin:0;">
    <img src="{{ base_path }}/images/research-cover-ais-2024.jpg" alt="Journal cover" style="width:100%; height:auto;">
  </figure>
  <figure style="width:200px; margin:0;">
    <img src="{{ base_path }}/images/research-cover-aem-2022.png" alt="Journal cover" style="width:100%; height:auto;">
  </figure>
  <figure style="width:200px; margin:0;">
    <img src="{{ base_path }}/images/research-cover-ais-2022.png" alt="Journal cover" style="width:100%; height:auto;">
  </figure>
  <figure style="width:200px; margin:0;">
    <img src="{{ base_path }}/images/research-cover-jmcc-2019.png" alt="Journal cover" style="width:100%; height:auto;">
  </figure>
</div>

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

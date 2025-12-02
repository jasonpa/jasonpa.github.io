---
layout: splash
title: "Ryu Clinic Guide Center"
permalink: /guides/
header:
  overlay_image: /assets/images/sean-o-KMn4VEeEPR8-unsplash.jpg
  #overlay_filter: 0.5
toc: false
---
<!-- The section is automatically determined by the order field in each guide's front matter:

Order 10-19 → ICBC & Car Accident
Order 20-29 → Extended Health Benefits
Order 30-39 → Office & Workers
Order 40-49 → Sports & Active Lifestyle
Order 50-69 → Symptoms & Conditions
Order 70-79 → Philosophy & First Visit
Order 80-89 → Locations & Access
 -->

<link rel="stylesheet" href="{{ '/assets/css/guides.css' | relative_url }}">

<div class="guides-hero">
  <h1>Ryu Clinic Guides</h1>
  <p>Practical guides for ICBC car accidents, extended health benefits, office and sports pain, and what to expect at Ryu Clinic in Coquitlam & Vancouver.</p>
</div>

<div class="guides-grid">

  <!-- ICBC Guides -->
  <div class="guide-card">
    <h3>ICBC & Car Accident</h3>
    <p>Learn how to navigate ICBC coverage, delayed pain, and combining acupuncture with other therapies after a car accident.</p>
    <ul>
      {% assign icbc_guides = site.guides | where_exp: "g", "g.order >= 10" | where_exp: "g", "g.order < 20" | sort: "order" %}
      {% for guide in icbc_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="#guides-icbc" class="guide-card-link">View guides</a>
  </div>

  <!-- Benefits Guides -->
  <div class="guide-card">
    <h3>Extended Health Benefits</h3>
    <p>Make the most of your extended health benefits for acupuncture and long-term maintenance care.</p>
    <ul>
      {% assign benefit_guides = site.guides | where_exp: "g", "g.order >= 20" | where_exp: "g", "g.order < 30" | sort: "order" %}
      {% for guide in benefit_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="#guides-benefits" class="guide-card-link">View guides</a>
  </div>

  <!-- Office / Workers Guides -->
  <div class="guide-card">
    <h3>Office & Workers</h3>
    <p>Guides for office workers, shift workers and professionals dealing with neck, shoulder and fatigue issues.</p>
    <ul>
      {% assign office_guides = site.guides | where_exp: "g", "g.order >= 30" | where_exp: "g", "g.order < 40" | sort: "order" %}
      {% for guide in office_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="#guides-office" class="guide-card-link">View guides</a>
  </div>

  <!-- Sports Guides -->
  <div class="guide-card">
    <h3>Sports & Active Lifestyle</h3>
    <p>Support for runners, hikers and active adults who want to keep moving with less pain.</p>
    <ul>
      {% assign sports_guides = site.guides | where_exp: "g", "g.order >= 40" | where_exp: "g", "g.order < 50" | sort: "order" %}
      {% for guide in sports_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="#guides-sports" class="guide-card-link">View guides</a>
  </div>

  <!-- Symptoms Guides -->
  <div class="guide-card">
    <h3>Symptoms & Conditions</h3>
    <p>Understand common patterns such as headaches, digestion, women's health and seasonal pain.</p>
    <ul>
      {% assign symptom_guides = site.guides | where_exp: "g", "g.order >= 50" | where_exp: "g", "g.order < 70" | sort: "order" %}
      {% for guide in symptom_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="#guides-symptoms" class="guide-card-link">View guides</a>
  </div>

  <!-- Philosophy & First Visit -->
  <div class="guide-card">
    <h3>Philosophy & First Visit</h3>
    <p>Learn about Ryu Clinic's treatment philosophy and what to expect at your first visit.</p>
    <ul>
      {% assign philosophy_guides = site.guides | where_exp: "g", "g.order >= 70" | where_exp: "g", "g.order < 80" | sort: "order" %}
      {% for guide in philosophy_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="#guides-philosophy" class="guide-card-link">View guides</a>
  </div>

  <!-- Locations & Access -->
  <div class="guide-card">
    <h3>Locations & Access</h3>
    <p>Find out how to choose between Coquitlam Momentum and Vancouver Regen, and how to get here.</p>
    <ul>
      {% assign location_guides = site.guides | where_exp: "g", "g.order >= 80" | where_exp: "g", "g.order < 90" | sort: "order" %}
      {% for guide in location_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="#guides-locations" class="guide-card-link">View guides</a>
  </div>

</div>

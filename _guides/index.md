---
layout: default
title: "Ryu Clinic Guide Center"
permalink: /guides/
---

<link rel="stylesheet" href="{{ '/assets/css/guides.css' | relative_url }}">

<div class="guides-hero">
  <h1>Your Guide to Feeling Better</h1>
  <p>Whether you're recovering from a car accident, dealing with daily pain, or looking for natural solutions to stress and fatigue, these guides will help you understand your options and take the next step with confidence.</p>
</div>

<div class="guides-grid">

  <!-- ICBC Guides Order 10-19 -->
  <div class="guide-card">
    <h3>ICBC & Car Accident Recovery</h3>
    <p>After a car accident, pain and stress can feel overwhelming. Find out how to start your recovery, what ICBC covers, and how acupuncture can help you heal faster and get back to your life.</p>
    <ul>
      {% assign icbc_guides = site.guides | where_exp: "g", "g.order >= 10" | where_exp: "g", "g.order < 20" | sort: "order" %}
      {% for guide in icbc_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="{{ icbc_guides.first.url | relative_url }}" class="guide-card-link">View guides →</a>
  </div>

  <!-- Office / Workers Guides Order 30-39 -->
  <div class="guide-card">
    <h3>Office & Workplace Pain</h3>
    <p>Neck tension, shoulder knots, and afternoon headaches shouldn't be part of your workday. Discover how to relieve desk-related pain and feel more comfortable at work.</p>
    <ul>
      {% assign office_guides = site.guides | where_exp: "g", "g.order >= 30" | where_exp: "g", "g.order < 40" | sort: "order" %}
      {% for guide in office_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="{{ office_guides.first.url | relative_url }}" class="guide-card-link">View guides →</a>
  </div>

  <!-- Symptoms Guides Order 50-69 -->
  <div class="guide-card">
    <h3>Chronic Pain & Common Conditions</h3>
    <p>Living with ongoing pain is exhausting. Whether it's headaches, back pain, or women's health concerns, learn how acupuncture can offer natural, lasting relief.</p>
    <ul>
      {% assign symptom_guides = site.guides | where_exp: "g", "g.order >= 50" | where_exp: "g", "g.order < 70" | sort: "order" %}
      {% for guide in symptom_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="{{ symptom_guides.first.url | relative_url }}" class="guide-card-link">View guides →</a>
  </div>

  <!-- Benefits Guides Order 20-29 -->
  <div class="guide-card">
    <h3>Extended Health Benefits</h3>
    <p>Your benefits can cover more than you think. Learn how to maximize your extended health coverage for acupuncture and ongoing wellness care.</p>
    <ul>
      {% assign benefit_guides = site.guides | where_exp: "g", "g.order >= 20" | where_exp: "g", "g.order < 30" | sort: "order" %}
      {% for guide in benefit_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="{{ benefit_guides.first.url | relative_url }}" class="guide-card-link">View guides →</a>
  </div>

  <!-- Sports Guides Order 40-49 -->
  <div class="guide-card">
    <h3>Sports & Active Lifestyle</h3>
    <p>Don't let pain sideline you. Whether you're a runner, hiker, or weekend warrior, find out how to recover faster and stay active.</p>
    <ul>
      {% assign sports_guides = site.guides | where_exp: "g", "g.order >= 40" | where_exp: "g", "g.order < 50" | sort: "order" %}
      {% for guide in sports_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="{{ sports_guides.first.url | relative_url }}" class="guide-card-link">View guides →</a>
  </div>

  <!-- Philosophy & First Visit Order 70-79 -->
  <div class="guide-card">
    <h3>Your First Visit & Our Approach</h3>
    <p>Nervous about trying acupuncture? We'll walk you through exactly what to expect, answer your questions, and help you feel comfortable from the moment you arrive.</p>
    <ul>
      {% assign philosophy_guides = site.guides | where_exp: "g", "g.order >= 70" | where_exp: "g", "g.order < 80" | sort: "order" %}
      {% for guide in philosophy_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="{{ philosophy_guides.first.url | relative_url }}" class="guide-card-link">View guides →</a>
  </div>

  <!-- Locations & Access Order 80-89 -->
  <div class="guide-card">
    <h3>Locations & Booking</h3>
    <p>We have two convenient locations in Coquitlam and Vancouver. Find the clinic closest to you, check directions, and book your first appointment.</p>
    <ul>
      {% assign location_guides = site.guides | where_exp: "g", "g.order >= 80" | where_exp: "g", "g.order < 90" | sort: "order" %}
      {% for guide in location_guides %}
        <li><a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a></li>
      {% endfor %}
    </ul>
    <a href="{{ location_guides.first.url | relative_url }}" class="guide-card-link">View guides →</a>
  </div>

</div>

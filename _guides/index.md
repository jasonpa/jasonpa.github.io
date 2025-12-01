---
layout: guide
title: "Ryu Clinic Guide Center"
permalink: /guides/
---

<p>
  Practical guides for ICBC car accidents, extended health benefits, office and sports pain,
  and what to expect at Ryu Clinic in Coquitlam & Vancouver.
</p>

<!-- ICBC Guides (order 10–19 예시) -->
<section id="guides-icbc" class="guides-section">
  <h2>ICBC & Car Accident Guides</h2>
  <p>Learn how to navigate ICBC coverage, delayed pain, and combining acupuncture with other therapies after a car accident.</p>
  <ul>
    {% assign icbc_guides = site.guides | where_exp: "g", "g.order >= 10" | where_exp: "g", "g.order < 20" | sort: "order" %}
    {% for guide in icbc_guides %}
      <li>
        <a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a>
        {% if guide.short_description %}
          <p class="guide-desc">{{ guide.short_description }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

<!-- Benefits Guides (order 20–29 예시) -->
<section id="guides-benefits" class="guides-section">
  <h2>Extended Health Benefits Guides</h2>
  <p>Make the most of your extended health benefits for acupuncture and long-term maintenance care.</p>
  <ul>
    {% assign benefit_guides = site.guides | where_exp: "g", "g.order >= 20" | where_exp: "g", "g.order < 30" | sort: "order" %}
    {% for guide in benefit_guides %}
      <li>
        <a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a>
        {% if guide.short_description %}
          <p class="guide-desc">{{ guide.short_description }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

<!-- Office / Workers Guides (order 30–39 예시) -->
<section id="guides-office" class="guides-section">
  <h2>Office & Workers Guides</h2>
  <p>Guides for office workers, shift workers and professionals dealing with neck, shoulder and fatigue issues.</p>
  <ul>
    {% assign office_guides = site.guides | where_exp: "g", "g.order >= 30" | where_exp: "g", "g.order < 40" | sort: "order" %}
    {% for guide in office_guides %}
      <li>
        <a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a>
        {% if guide.short_description %}
          <p class="guide-desc">{{ guide.short_description }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

<!-- Sports Guides (order 40–49 예시) -->
<section id="guides-sports" class="guides-section">
  <h2>Sports & Active Lifestyle Guides</h2>
  <p>Support for runners, hikers and active adults who want to keep moving with less pain.</p>
  <ul>
    {% assign sports_guides = site.guides | where_exp: "g", "g.order >= 40" | where_exp: "g", "g.order < 50" | sort: "order" %}
    {% for guide in sports_guides %}
      <li>
        <a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a>
        {% if guide.short_description %}
          <p class="guide-desc">{{ guide.short_description }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

<!-- Symptoms Guides (order 50–69 예시) -->
<section id="guides-symptoms" class="guides-section">
  <h2>Symptoms & Conditions Guides</h2>
  <p>Understand common patterns such as headaches, digestion, women’s health and seasonal pain.</p>
  <ul>
    {% assign symptom_guides = site.guides | where_exp: "g", "g.order >= 50" | where_exp: "g", "g.order < 70" | sort: "order" %}
    {% for guide in symptom_guides %}
      <li>
        <a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a>
        {% if guide.short_description %}
          <p class="guide-desc">{{ guide.short_description }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

<!-- Philosophy & First Visit Guides (order 70–79 예시) -->
<section id="guides-philosophy" class="guides-section">
  <h2>Philosophy & First Visit Guides</h2>
  <p>Learn about Ryu Clinic’s treatment philosophy and what to expect at your first visit.</p>
  <ul>
    {% assign philosophy_guides = site.guides | where_exp: "g", "g.order >= 70" | where_exp: "g", "g.order < 80" | sort: "order" %}
    {% for guide in philosophy_guides %}
      <li>
        <a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a>
        {% if guide.short_description %}
          <p class="guide-desc">{{ guide.short_description }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

<!-- Locations & Access Guides (order 80–89 예시) -->
<section id="guides-locations" class="guides-section">
  <h2>Locations, Access & Booking Guides</h2>
  <p>Find out how to choose between Coquitlam Momentum and Vancouver Regen, and how to get here.</p>
  <ul>
    {% assign location_guides = site.guides | where_exp: "g", "g.order >= 80" | where_exp: "g", "g.order < 90" | sort: "order" %}
    {% for guide in location_guides %}
      <li>
        <a href="{{ guide.url | relative_url }}">{{ guide.nav_title | default: guide.title }}</a>
        {% if guide.short_description %}
          <p class="guide-desc">{{ guide.short_description }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>

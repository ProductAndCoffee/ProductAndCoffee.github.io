---
layout: default
title: Work
permalink: /
description: "Portfolio of Venkat Iyappan: selected product and AI systems work across strategy, execution, infrastructure, and workflow design."
portfolio: true
---

<div class="portfolio-hero">
  <h1 class="portfolio-title">Venkat Iyappan</h1>
  <p class="portfolio-hero-subtext">productandcoffee.github.io</p>
  <div class="portfolio-social-links">
    <a href="https://linkedin.com/in/productandcoffee" target="_blank" class="portfolio-social-link">LinkedIn</a>
    <a href="https://github.com/ProductAndCoffee" target="_blank" class="portfolio-social-link">GitHub</a>
  </div>
  <p class="portfolio-lede">
    Product leader building AI-accelerated products from strategy to shipped software. I combine product strategy, design judgment, and hands-on technical execution to turn ambiguous ideas into tested, high-quality products.
  </p>
</div>

{% assign visible_projects = site.data.portfolio_projects | where: "include_on_portfolio", true | sort: "rank" %}
{% assign capabilities = visible_projects | map: "capability" | compact | uniq %}

{% for capability in capabilities %}
<section class="portfolio-capability-section">
  <h2 class="portfolio-section-title">{{ capability }}</h2>
  <div class="portfolio-grid">
    {% assign cap_projects = visible_projects | where: "capability", capability %}
    {% for project in cap_projects %}
      {% include portfolio-project-card.html project=project variant=project.status %}
    {% endfor %}
  </div>
</section>
{% endfor %}

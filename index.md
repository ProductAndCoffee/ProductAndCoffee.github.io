---
layout: default
title: Work
permalink: /
description: "Portfolio of Venkat Iyappan: selected product and AI systems work across strategy, execution, infrastructure, and workflow design."
portfolio: true
---

<div class="portfolio-hero">
  <div class="portfolio-breadcrumb">Home / Work</div>
  <h1 class="portfolio-title">Venkat Iyappan</h1>
  <p class="portfolio-subtext" style="color: var(--portfolio-text-muted); font-size: 1.1rem; margin-top: -8px; margin-bottom: 16px;">productandcoffee.github.io</p>
  <div class="portfolio-hero-links" style="display: flex; gap: 16px; margin-bottom: 24px;">
    <a href="https://linkedin.com/in/productandcoffee" target="_blank" style="color: var(--portfolio-text-primary); font-family: var(--font-nav); text-decoration: underline; text-underline-offset: 4px; font-weight: 500;">LinkedIn</a>
    <a href="https://github.com/ProductAndCoffee" target="_blank" style="color: var(--portfolio-text-primary); font-family: var(--font-nav); text-decoration: underline; text-underline-offset: 4px; font-weight: 500;">GitHub</a>
  </div>
  <p class="portfolio-lede">
    Product leader building AI-accelerated products from strategy to shipped software. I combine product strategy, design judgment, and hands-on technical execution to turn ambiguous ideas into tested, high-quality products.
  </p>
</div>

{% assign visible_projects = site.data.portfolio_projects | where: "include_on_portfolio", true | sort: "rank" %}
{% assign featured_projects = visible_projects | where: "status", "featured" %}
{% assign supporting_projects = visible_projects | where: "status", "supporting" %}

<section>
  <h2 class="portfolio-section-title">Featured Work</h2>
  <div class="portfolio-grid">
    {% for project in featured_projects %}
      {% include portfolio-project-card.html project=project variant="featured" %}
    {% endfor %}
  </div>
</section>

<section>
  <h2 class="portfolio-section-title">Supporting Work</h2>
  <div class="portfolio-grid">
    {% for project in supporting_projects %}
      {% include portfolio-project-card.html project=project variant="supporting" %}
    {% endfor %}
  </div>
</section>


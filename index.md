---
layout: default
title: Work
permalink: /
description: "Portfolio of Venkat Iyappan: selected product and AI systems work across strategy, execution, infrastructure, and workflow design."
portfolio: true
---

<div class="portfolio-hero">
  <div class="portfolio-breadcrumb">HOME / WORK</div>
  <h1 class="portfolio-title">Venkat Iyappan</h1>
  <p class="portfolio-hero-subtext">productandcoffee.github.io</p>
  <div class="portfolio-social-links">
    <a href="https://www.linkedin.com/in/ivenkat/" target="_blank" class="portfolio-social-link">LinkedIn</a>
    <a href="https://github.com/ProductAndCoffee" target="_blank" class="portfolio-social-link">GitHub</a>
  </div>
  <p class="portfolio-lede">
    Product leader building AI-accelerated products from strategy to shipped software. I combine product strategy, design judgment, and hands-on technical execution to turn ambiguous ideas into tested, high-quality products.
  </p>
</div>

{% assign visible_projects = site.data.portfolio_projects | where: "include_on_portfolio", true | sort: "rank" %}

<section class="portfolio-projects-section">
  <h2 class="portfolio-section-title">Selected Projects</h2>
  <div class="portfolio-grid">
    {% for project in visible_projects %}
      {% include portfolio-project-card.html project=project variant=project.status %}
    {% endfor %}
  </div>
</section>

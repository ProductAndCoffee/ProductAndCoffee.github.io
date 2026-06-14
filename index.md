---
layout: default
title: Work
permalink: /
description: "Portfolio of Venkat Iyappan: selected product and AI systems work across strategy, execution, infrastructure, and workflow design."
portfolio: true
---

<div class="portfolio-hero">
  <div class="portfolio-breadcrumb">Home / Work</div>
  <h1 class="portfolio-title">Work</h1>
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

<section>
  <h2 class="portfolio-section-title">How I Work</h2>
  <div class="portfolio-grid">
    <div class="portfolio-card variant-supporting">
      <h3 class="portfolio-card-title" style="font-size: 1.5rem;">AI-Augmented Execution</h3>
      <p class="portfolio-card-oneliner" style="font-size: 1rem;">AI as an execution multiplier, not a substitute for product judgment.</p>
      <div class="portfolio-card-evidence">
        <p>I use AI to accelerate PRDs, architecture reviews, code scaffolding, automated tests, debugging, and iteration. This allows me to move from ambiguous domains into tested, high-quality products faster, while retaining ownership of the final output and quality.</p>
      </div>
    </div>
    <div class="portfolio-card variant-supporting">
      <h3 class="portfolio-card-title" style="font-size: 1.5rem;">Quality & Craft</h3>
      <p class="portfolio-card-oneliner" style="font-size: 1rem;">Deterministic quality bar across design, code, and user experience.</p>
      <div class="portfolio-card-evidence">
        <p>A product must look premium and function flawlessly. I emphasize specification-first development, rigorous test coverage, clean design systems, and responsive architectures to ensure speed-to-value without compromising trust or reliability.</p>
      </div>
    </div>
    <div class="portfolio-card variant-supporting">
      <h3 class="portfolio-card-title" style="font-size: 1.5rem;">Product & Strategy</h3>
      <p class="portfolio-card-oneliner" style="font-size: 1rem;">Turning ambiguity into clear strategy.</p>
      <div class="portfolio-card-evidence">
        <p>I focus on understanding the core user job, identifying growth loops, and architecting products that solve real problems. Strategy is only as good as its execution, so I stay hands-on from initial concept to shipped software.</p>
      </div>
    </div>
  </div>
</section>

<section style="margin-bottom: 64px; text-align: center;">
  <h2 class="portfolio-section-title">Let's Connect</h2>
  <p class="portfolio-lede" style="margin: 0 auto 24px auto;">I'm always open to discussing product strategy, AI workflows, or new opportunities.</p>
  <div class="portfolio-card-links" style="justify-content: center;">
    <a href="https://linkedin.com/in/productandcoffee" target="_blank" style="font-size: 1.1rem;">LinkedIn</a>
    <a href="https://github.com/ProductAndCoffee" target="_blank" style="font-size: 1.1rem;">GitHub</a>
  </div>
</section>

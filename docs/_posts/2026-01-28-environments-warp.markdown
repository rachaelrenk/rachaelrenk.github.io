---
layout: post
title: "Cloud Agent Environments"
date: 2026-01-28
---

`👥 Developers` `🎯 Technical understanding` `📅 2026`

**Explained the mental model behind Warp's cloud agent environments, helping developers understand when they need one, what it contains, and how it fits into an agent run.**

### Impact

This conceptual, source-of-truth guide explains how environments give cloud agents a repeatable container, repositories, and setup for every run. The article distinguishes environments from related concepts such as hosts, agent profiles, rules, MCP servers, and per-run context, giving developers a clearer mental model for configuring cloud agent workflows.

### At a Glance

<div class="work-sample-grid">
  <div class="fact-card">
    <strong>Audience</strong>
    <p>Developers and DevOps engineers using Warp's cloud agents</p>
  </div>

  <div class="fact-card">
    <strong>Goal</strong>
    <p>Explain what environments are, when to use them, and how they fit into cloud agent runs</p>
  </div>

  <div class="fact-card">
    <strong>Collaboration</strong>
    <p>Product, Engineering</p>
  </div>

  <div class="fact-card">
    <strong>Tools</strong>
    <p>Git, Markdown, Warp</p>
  </div>
</div>

### View the Work

<div class="artifact-links">
  🔗 <a href="https://docs.warp.dev/platform/environments" target="_blank">View live documentation</a>

  📷 <a href="https://github.com/rachaelrenk/rachaelrenk.github.io/blob/portfolio_1/docs/assets/pdf/Environments_Warp.pdf" target="_blank">View PDF</a>
</div>

<details>
<summary><strong>Behind the work</strong> (click to expand)</summary>

<p><strong>Context:</strong></p>
<p>
Cloud agent environments define the repeatable runtime configuration for a Warp cloud agent run. The challenge was to explain a new and fairly abstract platform concept without requiring readers to understand the underlying architecture first. The guide needed to answer three questions clearly: what an environment is, what belongs inside one, and how it relates to the other components of a cloud agent run.
</p>

<p><strong>Activities:</strong></p>
<ul>
  <li>Developed the conceptual information architecture around the reader's mental model rather than the product's underlying implementation</li>
  <li>Defined clear distinctions between environments, hosts, agent profiles, rules, MCP servers, and per-run context</li>
  <li>Created a decision framework to help readers determine when an environment is appropriate and when a local run is sufficient</li>
  <li>Explained the runtime flow of a cloud agent run and how the environment contributes to it</li>
  <li>Validated technical concepts and examples through hands-on investigation and collaboration with product and engineering</li>
  <li>Separated conceptual explanation from procedural configuration content so each page could serve a clearer purpose</li>
</ul>

</details>

---
layout: post
title: "Designing Agent-Friendly Documentation"
date: 2026-06-29
---

`👥 Developers + AI agents` `🎯 Retrieval-ready docs` `📅 2026`

As AI agents become a primary interface for software, documentation has to work for both the people who read it and the agents that retrieve and reason over it. At Warp, I adapted a modern docs system for AI-native workflows, pairing durable design principles with recurring evaluation.

### The problem

Traditional docs are tuned for humans: prose, visual layout, and context the reader fills in. Agents consume docs as structured data, so what makes documentation *agent*-friendly is largely architectural:

* **Explicit structure** instead of implicit, visual-only hierarchy
* **Semantic organization** that groups related concepts predictably
* **Canonical concepts**, one authoritative page per idea, not scattered duplicates
* **Strong internal linking** so relationships are traversable, not just implied
* **Low ambiguity**, consistent terms with single, defined meanings
* **Predictable navigation** an agent can follow without guessing

Human-readable is not automatically agent-readable.

### At a glance

<div class="work-sample-grid">
  <div class="fact-card">
    <strong>Audience</strong>
    <p>Developers and the AI agents retrieving and reasoning over the docs</p>
  </div>
  
  <div class="fact-card">
    <strong>Goal</strong>
    <p>Make docs reliably useful for retrieval, reasoning, and task completion</p>
  </div>
  
  <div class="fact-card">
    <strong>Collaboration</strong>
    <p>Engineering, Growth, DevEx</p>
  </div>
  
  <div class="fact-card">
    <strong>Tools</strong>
    <p>Astro Starlight, llms.txt, <a href="https://afdocs.dev">AFDocs</a>, Git/GitHub, Warp (agentic AI)</p>
  </div>
</div>

### Principles

Agent-friendliness is an architectural property, not a writing trick. A few principles make retrieval and reasoning work by design.

<figure class="flow-diagram-figure">
  <div class="flow-diagram flow-diagram--vertical">
    <div class="flow-step">Information architecture</div>
    <div class="flow-arrow">↓</div>
    <div class="flow-step">Terminology</div>
    <div class="flow-arrow">↓</div>
    <div class="flow-step">Internal links</div>
    <div class="flow-arrow">↓</div>
    <div class="flow-step">Canonical concepts</div>
    <div class="flow-arrow">↓</div>
    <div class="flow-step">Structured pages</div>
    <div class="flow-arrow">↓</div>
    <div class="flow-step">Agent</div>
  </div>
  <figcaption><em>Agent-friendliness is built from the architecture up: each layer makes documentation more retrievable and more reliable for agents.</em></figcaption>
</figure>

* **Canonical concepts**: One concept, one authoritative page, so agents retrieve a single source of truth instead of reconciling duplicates.
* **Rich internal linking**: Agents navigate a graph, not a menu, so dense, accurate links make relationships traversable.
* **Structured information architecture**: A predictable hierarchy lets an agent locate and scope content reliably.
* **Consistent terminology**: One name, one meaning, so retrieval stays precise.
* **Retrieval-oriented writing**: Descriptive headings, lists, and one concept per section make content easy to chunk and extract.
* **Explicit context**: Define terms and state prerequisites so each page stands on its own.

These principles are durable; they hold regardless of which model or tool is reading the docs.

### Evaluation

Recurring checks measure agent-friendliness and track it over time:

* **[AFDocs audit](https://github.com/warpdotdev/docs/tree/main/.agents/skills/afdocs-audit)**: A weekly agent-friendliness scorecard with per-check scores and trend tracking, so regressions surface quickly.
* **AEO and [cross-link audits](https://github.com/warpdotdev/docs/tree/main/.agents/skills/aeo_crosslink_audit)**: Answer-engine optimization and relationship-graph coverage that catch orphaned pages and weak linking.
* **[llms.txt](https://docs.warp.dev/llms.txt)**: A machine-readable index that points agents to the full docs in markdown.
* **Search and discoverability**: Navigation and findability checks that keep content reachable.

How these checks actually run, on a schedule and feeding results back into the system, is the subject of the [Documentation Software Factory](/2026/06/29/documentation-software-factory-warp.html) page.

### Continuous improvement

Agent-friendliness compounds. The [Documentation Software Factory](/2026/06/29/documentation-software-factory-warp.html) runs these evaluations on a recurring cadence and turns the findings into improvements: the [skills](https://github.com/warpdotdev/docs/tree/main/.agents/skills) and [templates](https://github.com/warpdotdev/docs/tree/main/.agents/templates) that produce the docs evolve, and each pass leaves them more agent-ready than the last.

### Outcomes

* Improved AI discoverability of the documentation
* Stronger semantic relationships between pages
* Better, more predictable navigation
* Fewer orphaned pages
* Higher answer quality for agent and search queries
* More reusable, canonical concepts

### Lessons learned

* AI agents reward good information architecture more than polished prose.
* Retrieval quality depends more on structure than on writing style.
* Human-readable documentation is not automatically agent-readable.
* Continuous evaluation is more valuable than one-time optimization.

### Related projects

* [Documentation Software Factory](/2026/06/29/documentation-software-factory-warp.html): the recurring evaluations and automation that keep the docs improving.
* [Documentation Operating System](/2026/05/02/documentation-operating-system-warp.html): the architecture, workflows, and templates these principles build on.

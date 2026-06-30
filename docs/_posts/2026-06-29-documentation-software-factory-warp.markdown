---
layout: post
title: "Documentation Software Factory"
date: 2026-06-29
---

`👥 Docs team + AI agents` `🎯 Continuous docs improvement` `📅 2026`

Traditional documentation systems require humans to continually identify problems and update guidance. I designed the **Documentation Software Factory** to automate that feedback cycle using scheduled AI agents, recurring audits, telemetry, and human review to continuously improve documentation quality and discoverability.

### Problem

A documentation operating system establishes architecture, workflows, templates, validation, and governance, but none of it stays current on its own. Left unattended, even well-built docs decay:

* **Content drifts** as the product moves faster than manual updates
* **Stale links** and broken redirects that erode trust
* **Inconsistent terminology** creeping back in across contributors
* **Declining discoverability** in search and navigation
* **AI answerability gaps**, content humans can read but agents can't reliably use
* **Manual maintenance** that scales with headcount instead of the product

The operating system answers "how do we produce good docs?"; the Software Factory answers the harder follow-up: "how do we keep all of it good over time?"

### At a glance

<div class="work-sample-grid">
  <div class="fact-card">
    <strong>Audience</strong>
    <p>Docs operations team and the agents maintaining the docs</p>
  </div>
  
  <div class="fact-card">
    <strong>Goal</strong>
    <p>Automate the feedback cycle so quality improves continuously</p>
  </div>
  
  <div class="fact-card">
    <strong>Collaboration</strong>
    <p>Engineering, Growth, DevEx</p>
  </div>
  
  <div class="fact-card">
    <strong>Tools</strong>
    <p>Warp (agentic AI), scheduled cloud agents, Git/GitHub, Python, telemetry</p>
  </div>
</div>

### Architecture

The Software Factory is built on **outer loops**: a repeatable pattern where an inner loop does the work and emits signals, those signals accumulate in a structured log, and a scheduled outer-loop agent reads the log to propose improvements to the skills, templates, and guidance that drove the work. Every pass through the loop makes the next one better.

<figure class="flow-diagram-figure">
  <div class="flow-diagram">
    <div class="flow-step">Inputs<span>telemetry, audit logs, PR feedback</span></div>
    <div class="flow-arrow">→</div>
    <div class="flow-step">Agents<span>scheduled cloud agents</span></div>
    <div class="flow-arrow">→</div>
    <div class="flow-step">Evaluation<span>AFDocs, AEO, SEO, 404</span></div>
    <div class="flow-arrow">→</div>
    <div class="flow-step">Human review<span>draft PRs, approvals</span></div>
    <div class="flow-arrow">→</div>
    <div class="flow-step">Updated skills<span>templates and guidance</span></div>
    <div class="flow-arrow">→</div>
    <div class="flow-step">Stronger docs</div>
  </div>
  <figcaption><em>The outer-loop feedback cycle: signals flow from telemetry and audits through scheduled agents and human review, back into the skills that produce the docs.</em></figcaption>
</figure>

#### Core systems

The really valuable part isn't any single audit: it's the architecture that coordinates a set of specialized agents so the whole platform improves over time.

* **Outer loops**: The coordinating pattern. Inner loops emit signals; [scheduled outer-loop agents](https://github.com/warpdotdev/docs/tree/main/.agents/skills/improve-drafting-skills) read the accumulated signals and propose targeted edits to the underlying skills and templates, so improvements compound instead of resetting each cycle.
* **Scheduled cloud agents**: Recurring agents (for example, monthly and quarterly) run unattended, evaluate the docs, and open draft PRs. Now maintenance is a cadence rather than a fire drill.
* **Evaluation audits**: A family of specialized checks spanning agent-friendliness ([AFDocs](https://github.com/warpdotdev/docs/tree/main/.agents/skills/afdocs-audit)), answer-engine optimization ([AEO](https://github.com/warpdotdev/docs/tree/main/.agents/skills/aeo_crosslink_audit)), [SEO](https://github.com/warpdotdev/docs/tree/main/.agents/skills/docs-seo-audit), cross-link coverage, and [404 detection](https://github.com/warpdotdev/docs/tree/main/.agents/skills/weekly-404-monitor), each emitting structured signals instead of one-off reports.
* **Signal logs and telemetry**: Every run appends structured records to a shared [log layer](https://github.com/warpdotdev/docs/tree/main/.agents/logs). Accumulated telemetry is what lets agents act on patterns ("this rule is violated repeatedly") rather than isolated events.
* **Redirect generation**: High-confidence fixes, such as redirects for recurring 404s, are drafted automatically from audit data and proposed for review.
* **Skill improvement**: The highest-leverage output. The loops fix pages _and_ improve the reusable skills and templates that generate and review every future page.

📸 See the loops, skills, and signal logs live in [Warp's open-source docs repo](https://github.com/warpdotdev/docs/tree/main/.agents).

### Human in the loop

Automation proposes; humans decide. Every outer-loop agent opens its work as a **draft PR that requires human review; nothing auto-merges**. Agents handle detection, pattern analysis, and drafting; humans approve the architectural and editorial decisions that define what "good" means. That keeps the factory fast and self-improving without ceding judgment.

### Outcomes

* Continuous improvement replaces periodic cleanup. Docs get better between releases, not just during them.
* Docs become increasingly agent-friendly as AFDocs and AEO signals feed back into the templates.
* Maintenance shifts from manual work to recurring evaluation, so effort scales with the product instead of headcount.
* Reusable skills and templates improve over time, compounding quality across every future contribution.

### Lessons learned

* Durable quality comes from improving the system that produces the work, not from fixing the work piece by piece.
* Signals only help if they accumulate. Structured logs turn isolated runs into trends agents can act on.
* Automation earns trust when humans stay the approvers; draft-PR review keeps speed and judgment together.

### Related projects

* [Documentation Operating System](/2026/05/02/documentation-operating-system-warp.html): the architecture, workflows, templates, and validation that the Software Factory keeps current.

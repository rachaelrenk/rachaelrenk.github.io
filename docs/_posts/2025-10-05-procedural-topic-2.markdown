---
layout: post
title: "Procedural Topic (2)"
date: 2025-10-05
---

## Finding the Object ID for Your Entra OIDC Application – GitHub

**Reduced setup friction and support escalations by documenting a critical but previously undocumented prerequisite for OIDC token configuration.**

`👥 Enterprise Admins` `🎯 Reduced support tickets` `📅 2025`

### Impact

This procedural article filled a critical documentation gap for enterprise administrators configuring token lifetime policies for GitHub Enterprise Managed Users. By providing a validated workflow and example Graph API query, the article reduced setup friction and lowered support escalations related to OIDC session lifetime configuration. The content also improved cross-product accuracy by aligning GitHub's instructions with Microsoft's current Entra documentation and API behavior.

### At a Glance

<div class="work-sample-grid">
  <div class="fact-card">
    <strong>Audience</strong>
    <p>Enterprise administrators managing IAM for GitHub Enterprise Cloud</p>
  </div>
  
  <div class="fact-card">
    <strong>Goal</strong>
    <p>Document missing prerequisite step; reduce configuration errors; align with Microsoft standards</p>
  </div>
  
  <div class="fact-card">
    <strong>Collaboration</strong>
    <p>Subject matter experts, Microsoft documentation team</p>
  </div>
  
  <div class="fact-card">
    <strong>Tools</strong>
    <p>Git/GitHub, Markdown, Liquid, YAML, docs-as-code</p>
  </div>
</div>

### View the Work

<div class="artifact-links">
  🔗 <a href="https://docs.github.com/en/enterprise-cloud@latest/admin/managing-iam/configuring-authentication-for-enterprise-managed-users/finding-the-object-id-for-your-entra-oidc-application" target="_blank">View live documentation</a>
  
  📷 <a href="https://github.com/rachaelrenk/rachaelrenk/blob/678cd4c94a5698823731ee740c02534ac820adca/images/Finding-the-object-ID-for-your-Entra-OIDC-application-GHEC.pdf" target="_blank">View PDF</a>
  
  📷 <a href="#screenshots">View screenshots</a>
</div>

<p><details id="screenshots"><summary><strong>Screenshots</strong> (click to expand)</summary>
<p><img src="https://github.com/rachaelrenk/rachaelrenk/blob/main/images/Finding-the-object-ID-for-your-Entra-OIDC-application-GHEC-1.png?raw=true" style="border: 1px solid black" alt="First page showing procedural steps for locating Entra OIDC object ID" width="75%"/></p>

<p><img src="https://github.com/rachaelrenk/rachaelrenk/blob/main/images/Finding-the-object-ID-for-your-Entra-OIDC-application-GHEC-2.png?raw=true" style="border: 1px solid black" alt="Second page showing example Graph API query" width="75%"/></p>
<p><i>Screenshots captured October 2025.</i></p>
</details></p>

<details>
<summary><strong>Behind the work</strong> (click to expand)</summary>

<strong>>Context:</strong>

Enterprise administrators configuring Enterprise Managed Users (EMU) with Microsoft Entra OIDC needed to locate the object ID for their OIDC application—a prerequisite for setting token lifetime policies. This essential step was undocumented, causing setup delays and support escalations. The article is part of the larger EMU documentation set, which helps administrators integrate external identity providers like Entra ID and PingFederate.

<strong>Activities:</strong>

<ul>
<li>Collaborated with subject matter experts to validate technical requirements and ensure accuracy</li>
<li>Researched, tested, and verified steps by navigating Microsoft Entra UI and API workflows</li>
<li>Authored task-oriented procedures with concrete examples tailored for enterprise administrators</li>
<li>Created sample Graph API query to reduce trial-and-error during implementation</li>
<li>Reviewed and revised content to align terminology and style with both GitHub and Microsoft documentation standards</li>
</details>
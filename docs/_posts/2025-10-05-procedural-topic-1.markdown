---
layout: post
title:  "Procedural Topic (1)"
date:   2025-10-05 14:27:46 -0600
---

## Setting up an organization  - GitHub
This procedural topic guides new enterprise administrators through the process of adding organizations to their enterprise accounts. I authored this topic as part of the broader [GitHub Enterprise Onboarding Guide](/2025/10/06/enterprise-onboarding-guide.html) initiative.

### Artifacts
**"Setting up an organization"**
* [View the PDF.](https://github.com/rachaelrenk/rachaelrenk/blob/eb14eb14dab1e665dd9aa9061f4cfeed95db7af2/images/setting-up-an-organization.pdf) 📷

<p><details><summary><b>Screenshot</b> (click to expand)</summary>
<p><img src="https://github.com/rachaelrenk/rachaelrenk/blob/main/images/setting-up-an-org-1.png?raw=true" style="border: 1px solid black" alt="Enterprise onboarding guide" /></p>
</details></p>

#### Context
This article supports enterprise administrators during the early onboarding phase of the customer journey. The procedure addresses a key step in enterprise configuration: establishing organizational structure, roles, and ownership. The goal was to clarify a complex process involving conditional steps (based on enterprise type and account status) and ensure that administrators could complete setup without support intervention.

**Activities:**

* Conducted hands-on testing to validate each step and confirm UI behavior
* Structured content for clarity and logical flow, reflecting two possible paths ("create new" vs. "invite existing")
* Authored clear, step-by-step instructions supported by plain language and consistent formatting
* Linked related topics across the onboarding documentation to reinforce information flow and minimize redundancy

### Impact
Improved user comprehension and task success during enterprise setup by reducing confusion around organizational management and account constraints. The article became a key procedural reference in the enterprise onboarding flow, helping customers self-serve critical configuration steps and reducing dependency on support.

### Tools and skills
* Docs-as-code
* Git/GitHub
* Markdown
* Liquid
* CI/CD
* YAML


## Finding the object ID for your Entra OIDC application - GitHub
This procedural topic helps enterprise administrators locate the object ID for their Microsoft Entra OIDC app, a prerequisite for configuring token lifetime policies for managed users.

### Artifacts
**"Setting up an organization"**
* [View the live docs.](https://docs.github.com/en/enterprise-cloud@latest/admin/managing-iam/configuring-authentication-for-enterprise-managed-users/finding-the-object-id-for-your-entra-oidc-application?search-overlay-input=migrating+your+enterprise#using-microsoft-entra-id-admin-center-to-find-your-object-id) 🔗
* [View the PDF.](https://github.com/rachaelrenk/rachaelrenk/blob/678cd4c94a5698823731ee740c02534ac820adca/images/Finding-the-object-ID-for-your-Entra-OIDC-application-GHEC.pdf)📷 _PDF captured Oct 2025._

<p><details><summary><b>Screenshot</b> (click to expand)</summary>
<p><img src="https://github.com/rachaelrenk/rachaelrenk/blob/main/images/Finding-the-object-ID-for-your-Entra-OIDC-application-GHEC-1.png?raw=true" style="border: 1px solid black" alt="First page of the article" /></p>

<p><img src="https://github.com/rachaelrenk/rachaelrenk/blob/main/images/Finding-the-object-ID-for-your-Entra-OIDC-application-GHEC-2.png?raw=true" style="border: 1px solid black" alt="Second page of the article" /></p>
</details></p>

#### Context
This article supports enterprise administrators who are responsible for identitiy and access management (IAM) within GitHub Enterprise Cloud by clarifying na essential but previously undocumented step in the configuration workflow. The article is part of a larger Enterprise Managed Users (EMU) docset, which helps administrators integrate external identity provides such as Entra ID and PingFederate.

**Role:** Technical Writer

**Date:** 2024

**Activities:**

* Conducted hands-on testing to validate each step and confirm UI behavior
* Structured content for clarity and logical flow, reflecting two possible paths ("create new" vs. "invite existing")
* Authored clear, step-by-step instructions supported by plain language and consistent formatting
* Linked related topics across the onboarding documentation to reinforce information flow and minimize redundancy

### Impact
By providing a clear, validated workflow and example Graph API query, the article reduced setup friction for enterprise customers and lowered support escalations related to OIDC session lifetime configuration. It also improved cross-product accuracy by aligning GitHub’s instructions with Microsoft’s current Entra documentation and API behavior.

### Tools and skills
* Docs-as-code
* Git/GitHub
* Markdown
* Liquid
* CI/CD
* YAML

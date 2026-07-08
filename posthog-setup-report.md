# PostHog post-wizard report

The wizard has completed a deep integration of your portfolio site. Three new client-side events were added to `docs/_includes/posthog.html`, supplementing the three events that were already instrumented. All events fire via the existing PostHog JS snippet (loaded on production builds when `posthog_api_key` is set in `_config.yml`). No server-side SDK was added — this is a Jekyll static site and the JavaScript SDK is the correct integration path.

| Event | Description | File |
|---|---|---|
| `portfolio_link_click` | User clicks a portfolio card link on the homepage. | `docs/_includes/posthog.html` |
| `outbound_click` | User clicks an outbound link to GitHub or LinkedIn from any page. | `docs/_includes/posthog.html` |
| `software_factory_time_on_page` | Time in seconds a user spends on the Software Factory post before leaving. | `docs/_includes/posthog.html` |
| `post_time_on_page` | Time in seconds a user spends on any other portfolio post page before leaving. | `docs/_includes/posthog.html` |
| `resume_section_viewed` | User clicks a resume section navigation link (Skills, Experience, or Education). | `docs/_includes/posthog.html` |
| `email_click` | User clicks the email mailto link in the site footer. | `docs/_includes/posthog.html` |

## Next steps

We've built some insights and a dashboard for you to keep an eye on user behavior:

- [Analytics basics (wizard) — Dashboard](https://us.posthog.com/project/302575/dashboard/1819640)
- [Portfolio clicks by category (wizard)](https://us.posthog.com/project/302575/insights/828wfSkk)
- [Outbound clicks by destination (wizard)](https://us.posthog.com/project/302575/insights/ajLN9b43)
- [Post reading sessions (wizard)](https://us.posthog.com/project/302575/insights/j2CkPXyR)
- [Resume section engagement (wizard)](https://us.posthog.com/project/302575/insights/7jbT0vzP)
- [Email contact clicks (wizard)](https://us.posthog.com/project/302575/insights/dxpsn739)

## Verify before merging

- [ ] Run a full production build (`JEKYLL_ENV=production bundle exec jekyll build`) and confirm PostHog loads and events fire correctly in the browser console.
- [ ] Run the test suite — call sites that were rewritten or instrumented may need updated mocks or fixtures.

### Agent skill

We've left an agent skill folder in your project. You can use this context for further agent development when using Claude Code. This will help ensure the model provides the most up-to-date approaches for integrating PostHog.

# FlareWarden plugin for AI agents

Check whether any website or service such as Stripe, AWS or GitHub is down, and monitor
your own sites, the services they depend on, cron jobs and status pages with
[FlareWarden](https://flarewarden.com), from your AI agent.

This repository holds one plugin for Claude Code, Cursor and Codex: the FlareWarden MCP
server (`https://mcp.flarewarden.com/mcp`) and ten skills that guide the agent through
common jobs.

## Install

**Claude Code**

```
/plugin marketplace add Flare-Warden/agent-plugins
/plugin install flarewarden@flarewarden
```

**Cursor and Codex** read the marketplace files in this repository
(`.cursor-plugin/marketplace.json` and `.agents/plugins/marketplace.json`). The plugin
also follows the Agent Plugins standard (`plugins/flarewarden/plugin.json`).

**Any other MCP client:** connect to `https://mcp.flarewarden.com/mcp` (streamable HTTP).

## What it does

**No account needed:**

- Is a service such as Stripe or AWS down right now, going by its own status page and
  FlareWarden's checks.
- Does a website answer, checked from several regions at once.
- A preview of a site's monitoring: the services it depends on and their status now, when
  its certificate expires, its DNS, whether it is up, and what FlareWarden would set up.
  To go ahead, sign up at https://app.flarewarden.com/auth/register?utm_source=ai_assistant&utm_medium=mcp and come back: the
  agent signs in and sets up what the preview showed. Signing up carries nothing from the
  conversation.
- How FlareWarden works.

**With a FlareWarden account** (the first account question asks you to sign in):

- Set up monitoring for sites, the services they depend on, content checks, cron jobs, DNS
  records and certificates.
- Run status pages, post incidents and schedule maintenance.
- Report on uptime and incidents, manage the team, alert emails and webhooks.

The agent can do only what your account can do on the website. New monitors are shown to
you as a plan and created only after you confirm. Incident posts and maintenance windows
are drafted first and published only when you say so. API tokens for dependency checks
are entered on a FlareWarden page, never in the chat. Deleting monitors or status pages,
and billing, stay in the dashboard.

## Skills

| Skill | Use it to |
| --- | --- |
| `checking-service-status` | Find out whether a website or service is down. No account needed. |
| `setting-up-website-monitoring` | Start monitoring a site, with its dependencies and content checks. |
| `onboarding-client-portfolio` | Set up an agency's client sites, grouped per client, with client invitations. |
| `writing-uptime-reports` | Write uptime and SLA reports from your account's figures. |
| `monitoring-cron-jobs` | Watch scheduled jobs with a heartbeat the job pings. |
| `triaging-incidents` | Check whether an outage was real, what caused it, and what to post. |
| `running-status-pages` | Create a public status page and change its settings, custom domain and components. |
| `monitoring-third-party-dependencies` | Watch the services a site relies on: which components and regions, and how serious each is. |
| `watching-dns-and-certificates` | Get alerts when DNS records or certificates change, stop resolving or near expiry. |
| `managing-alerts-and-team` | Invite people, change roles, choose your alert emails, and connect Slack, Discord, Google Chat, Microsoft Teams or webhooks. |

## Links

- Documentation: https://flarewarden.com/docs
- Privacy policy: https://flarewarden.com/privacy
- Terms: https://flarewarden.com/terms
- Support: https://flarewarden.com/contact or support@flarewarden.com

## License

MIT. See [LICENSE](LICENSE).

# FlareWarden plugin for AI agents

Check whether any website or service such as Stripe, AWS or GitHub is down, and monitor
your own sites, the services they depend on, cron jobs and status pages with
[FlareWarden](https://flarewarden.com), from your AI agent.

This repository holds one plugin for Claude Code, Cursor and Codex: the FlareWarden MCP
server (`https://mcp.flarewarden.com/mcp`) and six skills that guide the agent through
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
- What to monitor for a site, and how FlareWarden works.

**With a FlareWarden account** (the first account question asks you to sign in):

- Set up monitoring for sites, the services they depend on, content checks, cron jobs and
  DNS records.
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
| `setting-up-website-monitoring` | Monitor one site, its dependencies, content, DNS and a status page. |
| `onboarding-client-portfolio` | Set up an agency's client sites, grouped per client, with client invitations. |
| `writing-uptime-reports` | Write uptime and SLA reports from your account's figures. |
| `monitoring-cron-jobs` | Watch scheduled jobs with a heartbeat the job pings. |
| `triaging-incidents` | Check whether an outage was real, what caused it, and what to post. |

## Links

- Documentation: https://flarewarden.com/docs
- Privacy policy: https://flarewarden.com/privacy
- Terms: https://flarewarden.com/terms
- Support: https://flarewarden.com/contact or support@flarewarden.com

## License

MIT. See [LICENSE](LICENSE).

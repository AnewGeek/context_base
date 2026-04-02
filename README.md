# AITA Context Base

Knowledge base for AI agents and copilots working with the AITA platform.

## What is AITA?

AITA is a vertical B2B platform for managing the full lifecycle of renewable energy projects. It combines CRM, project management, dataroom, equipment catalog, financial modeling, AI tools and trading operations in a single ecosystem.

**Company:** AITA WORLD, S.L. (Spain)
**Markets:** ES, PL, UA, DE
**Focus:** Solar PV, BESS, Energy Hubs

---

## Repository Structure

| File | Size | Description |
|------|------|-------------|
| `01_AITA_FULL_CONTEXT.md` | 687 KB | Business model, monetization framework (4 layers, 8 user groups, 21 billing codes), ecosystem architecture, NDA, and 8 contract profiles (Developer, Investor, EPC Partner, Delivery Team, Project Lead, Sales Agent, Recruiter, Marketing) --- all in EN + UA |
| `02_PLATFORM_LIVE_STATE.md` | 7.5 KB | Live snapshot of the platform: 10 projects, 4 SPVs (129 MW), 559 leads, 12 funnels, deals, offers, tasks, alerts |
| `03_PLATFORM_FUNCTIONALITY.md` | 15 KB | Full description of 16 platform modules: Project Management, SPV, CRM, Deals, Offers, Orders, Invoices, Catalog, Dataroom, Tasks, Entity Graph, Analytics, AI features, Solar Design Tools, User Management, MCP Integration |

---

## How the files complement each other

```
01_FULL_CONTEXT        WHY & HOW we earn money (legal + business logic)
        |
02_LIVE_STATE          WHAT is currently in the system (real data)
        |
03_FUNCTIONALITY       WHAT the platform can do (modules & capabilities)
```

- **01** answers: what are the commission structures, contract terms, user roles, billing events
- **02** answers: how many projects, leads, deals exist right now, what are the critical alerts
- **03** answers: what API endpoints and features are available, what can be automated

---

## Usage

### For AI Agents (NotebookLM, Claude, GPT, etc.)
Load all three files as context sources. They provide comprehensive knowledge about the AITA ecosystem --- from business rules to live data to technical capabilities.

### For MCP Integration
The platform exposes 100+ tools via Model Context Protocol. See `03_PLATFORM_FUNCTIONALITY.md` section 2.16 for details.

### For Team Onboarding
Start with `01` for business context, then `03` for platform capabilities, then `02` for current state.

---

## Key Metrics (as of 2026-04-02)

| Metric | Value |
|--------|-------|
| Projects | 10 |
| SPVs | 4 |
| Total SPV Capacity | 129.3 MW |
| CRM Contacts | 100+ |
| Leads | 559 |
| Funnels | 12 |
| Active Deals | 1 |
| Offers | 4 |
| Orders | 57 |
| Products | 100+ |
| Open Tasks | ~40 |

---

## Updating

`02_PLATFORM_LIVE_STATE.md` should be regenerated periodically to reflect current platform data. Use the AITA MCP API to pull fresh snapshots.

`01` and `03` are updated when business model or platform functionality changes.

---

*Generated 2026-04-02 by Claude Code from AITA MCP API*

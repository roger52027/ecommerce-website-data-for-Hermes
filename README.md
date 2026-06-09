# Ecommerce Website Data — Ecommerce Store Search & Analytics (Hermes)

> Search 10M+ ecommerce stores and ecommerce websites. Get ecommerce data, Shopify store analytics, revenue trends, tech stack, and decision-maker contacts — all for free.

Powered by [EcCompass AI](https://eccompass.ai) — one of the world's largest DTC databases — this skill delivers *free, live data* on 10M+ ecommerce stores with 100+ analytics fields.

This is the **Hermes** build of the skill. It declares a `metadata.hermes` block in `SKILL.md` so Hermes can register tags and **auto-prompt for the `APEX_TOKEN`** on first use. Script paths use the `{baseDir}` placeholder, which Hermes substitutes with the installed skill directory.

## What You Can Do

Search Stores — "Find Shopify stores selling pet food with 10k+ Instagram followers"

Domain Analytics — "Show me ooni.com's GMV trend and tech stack"

Lead Contacts — "Get decision-maker emails for this brand"

## Setup

**100% Free. One-minute setup.**

### Install via Hermes Agent

**Option 1: Install from Skills Hub**
```bash
/skills install ecommerce-website-data
```
*(or run `hermes skills install ecommerce-website-data` in your CLI)*

**Option 2: Install directly from GitHub**
```bash
/skills install github:roger52027/ecommerce-website-data-for-Hermes
```
*(or run `hermes skills install github:roger52027/ecommerce-website-data-for-Hermes` in your CLI)*

Repository: https://github.com/roger52027/ecommerce-website-data-for-Hermes

When you first use the skill, Hermes automatically prompts you for your `APEX_TOKEN` (declared in the skill's `metadata.hermes.config`). Get your free token at [eccompass.ai](https://eccompass.ai) → Dashboard → API Access → Create Token.

## Quick Start

Hermes substitutes `{baseDir}` with the installed skill path:

```bash
# Search by keyword
python3 {baseDir}/scripts/query.py search "pet food"

# Search with country + platform filters
python3 {baseDir}/scripts/query.py search "coffee" --country CN --platform shopify

# Filter only (no keyword)
python3 {baseDir}/scripts/query.py search --country US --platform shopify --min-gmv 1000000

# Get full analytics for a domain
python3 {baseDir}/scripts/query.py domain ooni.com

# Historical GMV and traffic trends
python3 {baseDir}/scripts/query.py historical ooni.com

# Installed apps/plugins
python3 {baseDir}/scripts/query.py apps ooni.com

# LinkedIn contacts
python3 {baseDir}/scripts/query.py contacts ooni.com
```

## Data Coverage

Powered by ECcompass.ai — one of the world's largest DTC databases — this skill delivers free, monthly-updated live data on 10M+ global ecommerce stores.

| Metric | Value |
|--------|-------|
| Total domains | 10,000,000+ |
| Countries | 200+ |
| Platforms | Shopify, WooCommerce, Wix, Squarespace, BigCommerce and more |
| GMV data | 2023–2026 yearly + last 12 months |
| Social media | Instagram, TikTok, Twitter/X, YouTube, Facebook, Pinterest |
| Update frequency | Monthly |

## Requirements

- Python 3.6+
- Network access to `api.eccompass.ai`
- `APEX_TOKEN` (Hermes prompts for it on first use)

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/public/api/v1/search` | POST | Search domains with keyword, filters, ranges, and sorting |
| `/public/api/v1/domain/{domain}` | GET | Full analytics for a single domain |
| `/public/api/v1/historical/{domain}` | GET | Monthly GMV and traffic history (2023+) |
| `/public/api/v1/installed-apps/{domain}` | GET | Installed apps/plugins with vendor details |
| `/public/api/v1/contacts/{domain}` | GET | LinkedIn contacts (name, position, email) |

## Documentation

- [AI Instructions](SKILL.md) — How the agent uses this skill
- [API Schema](references/schema.md) — Full response format and field definitions
- [Usage Examples](references/examples.md) — Real-world scenarios with sample output

## License

Proprietary — [EcCompass AI](https://eccompass.ai)

## Support

For questions, issues, or feature requests, visit [EcCompass AI](https://eccompass.ai).

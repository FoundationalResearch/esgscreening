# @foundationalresearch/esgscreening

[![npm version](https://img.shields.io/npm/v/@foundationalresearch/esgscreening.svg)](https://www.npmjs.com/package/@foundationalresearch/esgscreening)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![AI Skill](https://img.shields.io/badge/AI%20Skill-ESG%20Screening-green.svg)]()
[![Financial Analysis](https://img.shields.io/badge/Domain-Financial%20Analysis-orange.svg)]()

A standalone AI skill package for **ESG (Environmental, Social, Governance) screening and analysis**. This package provides a comprehensive agent methodology for evaluating companies against standard sustainability frameworks, identifying material ESG risks and opportunities, and producing structured ESG ratings.

Unlike generic sustainability prompts, this package delivers a rigorous assessment framework: systematic evaluation across all three ESG pillars, mapping to established reporting standards (SASB, TCFD, GRI, UN SDGs, ISSB, EU Taxonomy), industry-specific materiality analysis, and a structured scoring system -- all grounded in institutional-grade ESG methodology.

## What's Included

| File | Purpose |
|------|---------|
| `SKILL.md` | Agent skill -- full 6-step ESG screening methodology for LLM agents |
| `references/frameworks.md` | Reference material -- comprehensive guide to ESG reporting frameworks (SASB, TCFD, GRI, UN SDGs, ISSB, EU Taxonomy) |

This package is designed to work with AI coding agents and financial analysis tools that support skill discovery via npm packages. The agent reads `SKILL.md` for methodology guidance and references the frameworks guide for detailed standard definitions and mapping criteria.

## 6-Step ESG Screening Methodology

The agent skill (`SKILL.md`) walks the LLM through a rigorous ESG assessment framework:

1. **Environmental Assessment** -- Evaluate climate and emissions (Scope 1/2/3 GHG emissions, intensity metrics, carbon reduction targets, SBTi commitments, physical and transition climate risk), resource management (energy consumption, renewable mix, water usage, waste and recycling, circular economy, biodiversity), and environmental governance (ISO 14001, litigation, stranded asset risk, supply chain standards).

2. **Social Assessment** -- Analyze workforce factors (employee satisfaction, diversity and inclusion, pay equity, health and safety, training investment), supply chain practices (code of conduct, modern slavery policies, auditing, fair trade), and community and product impact (product safety, data privacy, community investment, access and affordability, controversial products).

3. **Governance Assessment** -- Examine board structure (independence, diversity, CEO/Chair separation, refreshment, committee structure), executive compensation (pay-for-performance, ESG metrics in pay, say-on-pay results, CEO pay ratio, clawbacks), shareholder rights (dual-class shares, poison pills, proxy access, shareholder proposals, related-party transactions), and ethics and transparency (anti-corruption, whistleblower protections, lobbying disclosure, tax transparency, compliance record).

4. **Framework Mapping** -- Map findings to established ESG reporting frameworks including SASB industry-specific standards, TCFD climate disclosures, GRI comprehensive sustainability reporting, UN Sustainable Development Goals, and EU Taxonomy green activity classification.

5. **Materiality Assessment** -- Identify which ESG factors are financially material for the specific company and industry, using a sector-based materiality matrix that highlights the most critical factors for Energy, Technology, Financials, Healthcare, Consumer, and Industrials sectors.

6. **ESG Score and Rating** -- Synthesize all findings into a structured assessment with individual E, S, and G scores (1-5 scale), an overall weighted composite, trend direction (improving/stable/deteriorating), and a controversies summary.

## Framework Coverage

The `references/frameworks.md` file provides detailed reference material on six major ESG reporting frameworks:

### SASB (Sustainability Accounting Standards Board)

Industry-specific material ESG factors across 77 standards. Designed for investor decision-making with quantitative metrics focused on enterprise value impact. Now part of the IFRS Foundation under ISSB.

### TCFD (Task Force on Climate-Related Financial Disclosures)

Climate risk and opportunity disclosure structured around four pillars: Governance, Strategy, Risk Management, and Metrics & Targets. Includes scenario analysis guidance (well below 2C, 2C, and 4C+ scenarios) and risk categorization (transition risks and physical risks).

### GRI (Global Reporting Initiative)

Comprehensive sustainability reporting for all stakeholders using universal, sector, and topic standards. Applies double materiality -- assessing both the impact on the company and the company's impact on the world.

### UN SDGs (Sustainable Development Goals)

All 17 Sustainable Development Goals mapped to investment relevance, from poverty alleviation and clean energy to climate action and responsible consumption.

### ISSB (International Sustainability Standards Board)

Global baseline for sustainability disclosures through IFRS S1 (general requirements) and IFRS S2 (climate-related disclosures). Consolidates SASB and TCFD into a single global standard.

### EU Taxonomy

Classification system for environmentally sustainable activities across six environmental objectives: climate change mitigation, climate change adaptation, sustainable use of water, transition to circular economy, pollution prevention, and biodiversity protection.

## Materiality Assessment by Sector

The skill includes a sector-specific materiality matrix that identifies the most financially material ESG factors:

| Sector | Most Material ESG Factors |
|--------|--------------------------|
| Energy | Climate transition, emissions, safety, water |
| Technology | Data privacy, workforce diversity, e-waste |
| Financials | Governance, responsible lending, cyber security |
| Healthcare | Drug pricing, product safety, access |
| Consumer | Supply chain, labor practices, packaging |
| Industrials | Emissions, safety, water, circular economy |

This ensures the analysis focuses on what actually matters for each industry rather than applying a one-size-fits-all assessment.

## Usage

### Claude Code

Add the skill package as a dependency or install it globally:

```bash
npm install @foundationalresearch/esgscreening
```

The agent will discover the skill automatically and use it when users ask about ESG profiles, sustainability analysis, or responsible investing criteria. Example prompts:

- "What is Apple's ESG profile?"
- "Screen MSFT for ESG risks and sustainability"
- "Analyze the governance structure of Tesla"
- "How does ExxonMobil score on environmental metrics?"
- "Compare the ESG profiles of JPM and GS"
- "Is this company aligned with the UN SDGs?"

### Cursor

Install the package in your project:

```bash
npm install @foundationalresearch/esgscreening
```

Reference the skill in your Cursor rules or let the agent discover it from `node_modules`. The `SKILL.md` file provides the full ESG screening methodology and the `references/frameworks.md` file provides detailed framework definitions.

### Codex

Add the package to your project dependencies:

```bash
npm install @foundationalresearch/esgscreening
```

Codex agents can read the `SKILL.md` for step-by-step ESG analysis guidance and reference the frameworks guide for standard definitions and mapping criteria.

### Manual Usage

You can also reference the skill files directly without installing as an npm package:

```bash
# Clone the repository
git clone https://github.com/FoundationalResearch/esgscreening.git

# Point your agent to the skill directory
# The agent reads SKILL.md for methodology and references/frameworks.md for standards
```

## Output Format

The skill produces structured output containing:

1. **ESG Summary** -- One-paragraph overview of the company's ESG profile
2. **Environmental Score and Key Findings** -- E score (1-5) with supporting evidence
3. **Social Score and Key Findings** -- S score (1-5) with supporting evidence
4. **Governance Score and Key Findings** -- G score (1-5) with supporting evidence
5. **Materiality Matrix** -- Industry-specific material factors and their assessment
6. **Framework Alignment** -- Mapping to SASB and TCFD standards
7. **Controversies and Risks** -- Material ESG incidents, lawsuits, or red flags
8. **ESG Trend Assessment** -- Direction of ESG performance (improving, stable, or deteriorating)

## Important Notes

- **Data quality varies** -- ESG data is self-reported by companies and varies significantly in completeness and reliability. The skill notes data sources and limitations.
- **Greenwashing risk** -- The methodology emphasizes verified data, third-party audits, and specific measurable targets over vague commitments.
- **Materiality is industry-specific** -- What matters for a bank differs fundamentally from what matters for a mining company. The skill tailors its analysis accordingly.
- **ESG risk vs. ESG impact** -- The skill distinguishes between ESG risk (financial impact on the company) and ESG impact (the company's effect on the world).
- **Rating divergence** -- ESG ratings from different providers (MSCI, Sustainalytics, ISS) often disagree. The skill explains its own methodology transparently.

## Related Skills

Other financial analysis skill packages from FoundationalResearch:

- `@foundationalresearch/dcfvaluation` -- Discounted cash flow valuation with WACC calculation and scenario modeling
- `@foundationalresearch/creditanalysis` -- Credit risk assessment with rating methodology and financial covenant analysis
- `@foundationalresearch/technicalanalysis` -- Technical chart analysis with indicator glossary and pattern recognition
- `@foundationalresearch/earningscallanalysis` -- Earnings call transcript analysis with sentiment and key metrics extraction
- `@foundationalresearch/companalysis` -- Comparable company analysis with peer benchmarking and relative valuation

## Installation

```bash
npm install @foundationalresearch/esgscreening
```

Or add to your `package.json`:

```json
{
  "dependencies": {
    "@foundationalresearch/esgscreening": "^1.0.0"
  }
}
```

## Requirements

This skill works best with access to financial data tools for gathering ESG-related information:

- `search_filings` -- Searches SEC EDGAR for sustainability reports, proxy statements, and 10-K filings with ESG disclosures
- `search_news` -- Finds recent ESG-related news, controversies, and sustainability announcements

The agent skill (`SKILL.md`) can be used independently of these tools for methodology guidance, but access to filing and news data enables more comprehensive and evidence-based analysis.

## License

MIT -- see [LICENSE](./LICENSE) for details.

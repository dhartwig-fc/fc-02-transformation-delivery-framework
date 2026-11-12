[← Back to Portfolio](https://dhartwig-fc.github.io/dan-hartwig-portfolio/)

[LinkedIn](https://www.linkedin.com/in/dan-hartwig-financial-crime) | [GitHub Profile](https://github.com/dhartwig-fc)

# Financial Crime Transformation & Delivery Framework

---

## Executive Summary

The Financial Crime Transformation & Delivery Framework demonstrates how emerging financial crime threats can be transformed into operational capabilities through intelligence-led strategy, analytics development, governance, AI enablement and operational deployment.

The repository acts as the delivery and transformation layer supporting the wider Financial Crime Intelligence Platform, **NEXUS**.

Whilst supporting repositories focus on specific analytical capabilities, this repository focuses on the frameworks, operating models, governance structures and delivery approaches used to identify, prioritise, design, build and operationalise those capabilities.

The framework has now been applied end to end. NEXUS was built with it and is at Beta v2.2, in a test phase. [Where the programme stands](#where-the-programme-stands) gives the position. [The lifecycle in practice](#the-lifecycle-in-practice) shows how each step of the method was carried out.

The framework spans:

- Network Intelligence
- Trade-Based Money Laundering (TBML) Analytics
- Correspondent Banking Analytics
- Capital Markets Analytics
- Sanctions Exposure Analytics and Maritime Intelligence
- Emerging Threat Intelligence
- Detection Strategy
- AI-Enabled Financial Crime Operations

---

# Where the programme stands

*As of 12 November 2026. The live figures are on the NEXUS pages linked below. Test counts and defect counts change daily, so they are not repeated here.*

- **Built.** NEXUS runs detection on one resolved-entity substrate across all five crime families: network intelligence, TBML, sanctions, correspondent banking and capital markets. It has 57 typologies, each a governed product with authored doctrine. A fused investigator console sits over that substrate.
- **Operations layer.** A tamper-evident case event log is the system of record. The SAR lifecycle, SLA orchestration and QA oversight are all built on it.
- **At scale.** One governed batch runs over a synthetic estate of 9,889 entities, from daily feeds to operations decisions. A replay reproduces the run exactly.
- **Running on a schedule.** A living estate advances one business day every weekday morning, and has done since 16 October 2026. A weekly drift check re-runs the estate and compares the results.
- **Learning.** Threat intelligence now feeds back into the platform. An advisory can corroborate a typology, queue the cases built on it for re-review, or propose a new typology.
- **Being tested.** New features have been frozen since 19 October 2026 for a test phase of about twelve weeks, to about 11 January 2027. Only defect fixes and test work land, each against a pinned CI baseline.
- **Not yet deployed.** NEXUS is a reference build on synthetic demonstration data. The test phase ends in a go / no-go decision for a production-like pilot.

Live status:

- [Mission Status](https://dhartwig-fc.github.io/dan-hartwig-portfolio/projects/nexus/mission-status.html): what is built, in flight and next
- [Test Phase](https://dhartwig-fc.github.io/dan-hartwig-portfolio/projects/nexus/testing.html): progress by phase, defects and the baseline
- [Platform Roadmap](https://dhartwig-fc.github.io/dan-hartwig-portfolio/projects/nexus/platform-roadmap.html): the phase arc and what comes after the test phase
- [Stage Catalogue](https://dhartwig-fc.github.io/dan-hartwig-portfolio/projects/nexus/stage-catalogue.html): how each build shipped
- [Governance and Assurance Pack](https://dhartwig-fc.github.io/dan-hartwig-portfolio/projects/nexus/governance-pack.html): the ten sign-off documents and their status
- [Investigator Console](https://dhartwig-fc.github.io/dan-hartwig-portfolio/projects/nexus/runtime-demo/console.html): the public demo

---

# Relationship to Portfolio Showcase

The Financial Crime Intelligence Platform consists of multiple interconnected repositories, each serving a different purpose.

### Portfolio Site (dan-hartwig-portfolio)

The public executive showcase. It hosts the NEXUS pages: the investigator console demo, the published investigation cases, the Knowledge Centre, the data dictionary, the telemetry heartbeat, and the status and governance pages linked above.

### fc-01 Financial Crime Analytics Showcase

The original capability showcase repository: domain overviews for network intelligence, TBML, correspondent banking, capital markets, sanctions exposure and the AI investigator copilot. It was last updated in June 2026. The live showcase is now the portfolio site.

### fc-02 Transformation & Delivery Framework

Provides the methodology used to transform emerging threats into operational capabilities.

Focus areas include:

- Transformation
- Delivery
- Governance
- Operating Models
- Strategy
- Capability Development
- AI Enablement

### fc-10 NEXUS Platform and the Domain Repositories

The domain repositories hold the analytics for each crime family. The NEXUS core platform (fc-10) loads those analytics, runs them over one resolved-entity substrate, and publishes the results to the portfolio site through governed publishers. Emerging threat intelligence (fc-08) feeds into the platform.

```text
                 fc-08 Emerging Threat Intelligence
                    │  advisories linked to typologies
                    ▼
 ┌──────────────┬──────────────┬──────────────┬──────────────┬──────────────┐
 │ fc-03        │ fc-04        │ fc-05        │ fc-06        │ fc-07        │
 │ Network      │ TBML         │ Sanctions    │ Corr Banking │ Cap Markets  │
 │ Intelligence │ Analytics    │ Exposure     │ Analytics    │ Analytics    │
 └──────────────┴──────────────┴──────────────┴──────────────┴──────────────┘
                    │  analytics loaded by the platform
                    ▼
            fc-10 NEXUS core platform
                    │  governed publishers
                    ▼
            Portfolio site (public)

  Method and standards alongside:
  fc-02 Transformation & Delivery Framework   (this repository)
  fc-20 Canonical Intelligence Delivery Model (delivery standard)
```

---

# Financial Crime Transformation Mission

The framework demonstrates how financial institutions can transform threats into measurable business outcomes.

```text
External Threats
        ↓
Intelligence
        ↓
Strategy
        ↓
Capability Design
        ↓
Delivery
        ↓
Operations
        ↓
Governance
        ↓
Business Outcomes
```

---

# Capability Delivery Lifecycle

The framework demonstrates a repeatable capability delivery model.

```text
Threat Identified
        ↓
Threat Assessment
        ↓
Business Case
        ↓
Target State Design
        ↓
Capability Development
        ↓
Pilot
        ↓
Operational Deployment
        ↓
Performance Monitoring
        ↓
Continuous Improvement
```

---

# The lifecycle in practice

How each lifecycle step was carried out in NEXUS, with the honest gaps.

| Lifecycle step | In NEXUS |
|---|---|
| Threat Identified | fc-08 runs a scheduled sweep of regulator and law-enforcement publications. The owner approves each link from an advisory to a typology. An unknown pattern can be opened as a governed typology proposal |
| Threat Assessment | Doctrine is authored for every one of the 57 typologies and published in the Knowledge Centre |
| Business Case | **Not yet a formal artefact.** A capability briefing deck exists, private and shown on request |
| Target State Design | A canonical data dictionary (published). The Technical Specification and Target Operating Model are drafted for approval |
| Capability Development | Built as numbered stage packages, Stage 1 to Stage 568, from May to November 2026 (table below). Each package lands only when a pinned CI baseline holds |
| Pilot | A reference build on synthetic data: a bank-scale estate run as one governed batch, and a living estate that advances one business day every weekday |
| Operational Deployment | **Not yet.** The go / no-go for a production-like pilot is the exit of the current test phase |
| Performance Monitoring | A public telemetry heartbeat, a weekly drift check, and operations MI over the case event log |
| Continuous Improvement | The test phase: every defect is registered, and each fix lands with a failing test first. New intelligence that corroborates a typology queues its cases for re-review |

### Build history

NEXUS was delivered in fifteen eras. Each era is a run of numbered stages. The summary below comes from the NEXUS stage register, which is private.

| Era | Stages | What it delivered |
|---|---|---|
| E1 Pattern Factory foundations | 1–59 | Sample data, schema validation, and reusable network-intelligence patterns rendered from metadata. May–June 2026 |
| E2 Topology and reasoning engines | 60–99 | The metadata renderer, topology registry, layout strategies and the first reasoning engines. June 2026 |
| E3 Legacy intelligence engines | 100–176 | The previous platform generation, since retired from the shipping path |
| E4 Design documents | 177–286 | One design document per stage: workspace runtime, context and investigation services, the architecture baseline lock |
| E5 Gold standard and oracle validation | 287–299 | The gold-standard case layout and the defect governance every later defect runs under |
| E6 Canonical graph and runtime certification | 300–347 | The canonical renderer locked and the first runtime product certified |
| E7 The product contract | 348–399 | The product page as a governed contract: templates, metadata contracts, renderer audits |
| E8 The manufacturing pipeline | 400–426 | Manufacture as a pipeline: output contracts, provenance, regression harness, release bundles |
| E9 Visual language | 427–436 | Visual grammar, layout and routing, the semantic release gate, the cross-typology lock |
| E10 Derived product semantics | 437–532 | Each stage removed one thing a product asserted without deriving it |
| E11 The investigator console | 533–548 | The fused console over the shared estate |
| E12 Remediation and an honest baseline | 549–559 | The inherited failing baseline resolved to its root causes; the baseline became zero failures |
| E13 Tuning | 560 | A tuning studio over a population whose truth is known |
| E14 Operations and batch analytics | 561–563 | Case event log, SAR lifecycle, SLA and QA oversight, the world generator, the batch runner, daily feeds and ingestion |
| E15 The living platform and the learning loop | 564–568 | Scheduled runs, the threat-intelligence learning loop, the maritime case, the telemetry heartbeat |

---

# Transformation Framework

The assets listed under each discipline are the framework's asset *types*. [Toolkit Components](#toolkit-components) shows where each one exists today.

## 🧠 Intelligence

### Purpose

Identify, assess and prioritise emerging financial crime threats.

### Assets

- Emerging Threat Intelligence Repository
- Threat Catalogue
- Horizon Scanning Framework
- Intelligence Ecosystem
- Threat Assessment Framework

---

## 🎯 Strategy

### Purpose

Translate intelligence into business priorities and transformation objectives.

### Assets

- Business Case Framework
- Executive Board Presentation
- Target Operating Model
- Transformation Roadmap
- Benefits Realisation Framework

---

## 🏗️ Design

### Purpose

Convert threats into analytical and operational requirements.

### Assets

- Detection Strategy Library
- Threat-to-Detection Mapping
- Scenario Engineering
- Control Coverage Assessment
- Quantexa + AI Integration Blueprint
- Reference Architectures

---

## 🚀 Delivery

### Purpose

Build and validate analytical capabilities.

### Assets

- AML Alert Triage Prototype
- AI Investigator Copilot
- Python Analytics Prototype
- Proof of Concept Backlog
- Jira Delivery Pack

---

## ⚙️ Operations

### Purpose

Embed capabilities into financial crime workflows.

### Assets

- Investigation Frameworks
- Operational Playbooks
- Risk Scoring Frameworks
- Escalation Models
- Case Management Concepts

---

## 🏛️ Governance

### Purpose

Ensure capabilities remain explainable, effective and controlled.

### Assets

- AI Governance Framework
- Model Risk Management
- Explainability Controls
- Human-in-the-Loop Controls
- Calibration Frameworks

---

## 📈 Transformation Outcomes

- Improved Detection Effectiveness
- Reduced False Positives
- Enhanced Investigator Productivity
- Better Risk Prioritisation
- Improved Explainability
- Faster Capability Delivery
- Improved Governance
- Stronger Operational Effectiveness

---

# Emerging Threat Intelligence Integration

Emerging Threat Intelligence provides the strategic input into the transformation lifecycle.

This now runs. fc-08 sweeps the sources below on a schedule and turns each advisory into owner-reviewed links to the typologies it matches. NEXUS absorbs the approved links: a link to a known typology corroborates it and queues the cases built on it for re-review, and an unknown pattern can become a governed typology proposal. The same sweep feeds the *Fault Lines* newsletter. The [Threat Intelligence Walkthrough](https://dhartwig-fc.github.io/dan-hartwig-portfolio/projects/nexus/threat-intel/) follows one advisory from PDF to approved typology links.

### Intelligence Ecosystem

- FATF
- Europol
- FinCEN
- Wolfsberg Group
- FCA
- NCA
- OFAC
- OFSI
- Egmont Group
- OECD
- BIS
- World Economic Forum
- United Nations

### Emerging Threat Themes

- Artificial Intelligence Abuse
- Agentic AI
- Digital Assets
- Synthetic Identities
- Trade-Based Sanctions Evasion
- Complex Ownership Structures
- Professional Mule Networks
- Shadow Fleet Networks
- Supply Chain Manipulation
- Geopolitical Risk Corridors

### Intelligence Outputs

- Threat Assessments
- Threat Prioritisation
- Detection Strategies
- Analytics Opportunities
- Future Typologies
- Capability Roadmaps

---

# Toolkit Components

| # | Component | Category | Description | Where it lives today | Status |
|---|-----------|----------|-------------|----------------------|--------|
| 1 | AI-Enabled Investigator Copilot | AI | Alert summarisation and investigation support | fc-prot02 prototype; the NEXUS copilot case flow in the investigator console | Live for three showcase cases. Its wording is template-based; AI wording awaits owner approval |
| 2 | AML Alert Triage Prototype | Analytics | Alert scoring and prioritisation | fc-prot01 prototype; the NEXUS ranked alert table and task queue | Prototype, superseded by NEXUS |
| 3 | Financial Crime Risk Typology Library | Intelligence | Risk typology catalogue | NEXUS Knowledge Centre | Built: doctrine for all 57 typologies |
| 4 | Financial Crime Network Intelligence Library | Analytics | Entity resolution and network investigation patterns | fc-03 | Built: five foundation products and ten network typologies |
| 5 | Correspondent Banking Analytics Toolkit | Analytics | Nested relationships, pass-through and payment-flow analytics | fc-06 | Built: BA001–BA010 |
| 6 | Sanctions Exposure Analytics Toolkit | Analytics | Screening, exposure, ownership and maritime analytics | fc-05 | Built: SAN001–SAN009 and CMI010 |
| 7 | Trade Finance & TBML Analytics Toolkit | Analytics | TBML analytics and risk scoring | fc-04 | Built: TBML001–TBML011 and TBML002U |
| 8 | Capital Markets Surveillance Toolkit | Analytics | Market abuse analytics | fc-07 | Built: CM001–CM010 |
| 9 | Emerging Threat Intelligence Repository | Intelligence | Horizon scanning and threat assessment | fc-08 | Live: scheduled sweep feeding NEXUS |
| 10 | Detection Strategy Library | Detection Strategy | Threat-to-detection mapping | fc-09 | Planned: README only |
| 11 | AI Governance Framework | Governance | AI governance and controls | NEXUS governance pack: Detection Methodology and Independent Model Validation Report | Detection Methodology drafted for approval; validation report in preparation |
| 12 | Target Operating Model | Transformation | Future-state operating model | NEXUS governance pack (NEXUS-TOM-001); fc-20 operating model book | Drafted for approval |
| 13 | Transformation Roadmap | Transformation | Delivery planning | NEXUS Platform Roadmap | Published |
| 14 | Business Case & Value Framework | Transformation | Benefits and ROI framework | None yet | Not started |
| 15 | Executive Board Presentation | Transformation | Executive stakeholder materials | NEXUS capability briefing (17 slides) | Built; private, shown on request |
| 16 | Proof of Concept Backlog & Jira Pack | Delivery | Delivery artefacts and backlog management | In practice: numbered stage packages, a defect register and CI-gated pull requests on GitHub | Replaced in practice; no Jira pack |

---

# Repository Catalogue

| Repository | Visibility | Purpose |
|------------|------------|---------|
| dan-hartwig-portfolio | Public | Portfolio website, hosting the public NEXUS pages |
| fc_vision_notes_dhartwig | Private | Strategy notes and portfolio vision |
| fc-01-financial-crime-analytics-showcase | Public | Original capability showcase (last updated June 2026) |
| fc-02-transformation-delivery-framework | Public | Transformation and delivery framework (this repository) |
| fc-03-network-intelligence-library | Private | Entity resolution, network intelligence and foundation doctrine |
| fc-04-tbml-analytics-toolkit | Private | Trade analytics and TBML typologies |
| fc-05-sanctions-exposure-analytics-toolkit | Private | Sanctions exposure, evasion detection, ownership and maritime analytics |
| fc-06-correspondent-banking-analytics-toolkit | Public | Correspondent banking analytics |
| fc-07-capital-markets-analytics-toolkit | Public | Capital markets and surveillance analytics |
| fc-08-emerging-threat-intelligence | Public | Horizon scanning and threat intelligence |
| fc-09-detection-strategy-library | Public | Threat-to-detection mapping and scenario engineering (planned; README only) |
| fc-10-intelligence-repository-layer | Private | NEXUS core platform: substrate, detection, products, console, operations and the living estate |
| fc-20-canonical-intelligence-delivery-model | Private | Delivery standard: architecture, operating model, technical specification, interfaces, reference implementation and design rationale |
| fc-prot01-aml-alert-triage | Public | AML triage prototype |
| fc-prot02-ai-investigator-copilot | Public | AI-enabled Investigator Copilot prototype |
| fc-rm01-ai-transformation-roadmap | Public | Structured AI learning roadmap |
| fc-rm02-transformation-ai-lab | Public | AI lab building solutions using RAG, Agentic AI, MCP and automation |

---

# Portfolio Build Roadmap

| Status | Initiative |
|----------|----------|
| ✅ Complete | Portfolio Website |
| ✅ Complete | Transformation Framework |
| ✅ Complete | Showcase build |
| ✅ Complete | Network Intelligence Library |
| ✅ Complete | TBML Analytics Toolkit |
| ✅ Complete | Sanctions Exposure Analytics Toolkit |
| ✅ Complete | Correspondent Banking Analytics Toolkit |
| ✅ Complete | Capital Markets Analytics Toolkit |
| ✅ Live | Emerging Threat Intelligence |
| 🧪 Test phase | NEXUS platform: Beta v2.2; features frozen 19 October 2026 to about 11 January 2027 |
| 🚧 In preparation | Governance and assurance pack, including AI governance: 4 of 10 documents drafted for approval |
| Next | Investigator Workspace operational surface, after the test phase |
| Planned | Detection Strategy Library |

---

# Repository Purpose

This repository explains how financial crime capabilities are identified, prioritised, designed, delivered, governed and continuously improved.

It serves as the transformation and delivery framework underpinning the wider Financial Crime Intelligence Platform.

Unlike the showcase repository, this repository focuses on delivery methodology, governance, operating models, transformation frameworks and capability development.

---

## Intellectual Property Notice

This repository is intended as a public showcase of methodology, architecture, transformation frameworks and capability design.

Detailed analytical logic, scoring methodologies, calibration parameters, implementation code, operational playbooks and proprietary delivery artefacts remain private intellectual property.

Selected materials may be made available upon request.

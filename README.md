# NEXORYN: Evidence-Driven Package Metadata Integrity and Anomaly Assessment for Open-Source Software Supply Chains

> **Status:** Proposal stage. NEXORYN is a planned six-month feasibility project proposed for the NLnet Foundation's CodeSupply call. No verification rules, evaluation datasets or prototype have been published yet.

## About

Software Bills of Materials (SBOMs) and compliance tools often rely on package registry metadata, particularly **declared software licences** and **source repository links**. These fields may be missing, outdated or inconsistent with other available evidence. When copied into downstream tools, inaccurate metadata can undermine traceability and compliance assessments.

**NEXORYN** will assess the feasibility of transparent, evidence-driven checks for these two metadata fields, initially using selected **PyPI** releases. The project will define reusable core rules and explore how registry-specific mappings could support future application to ecosystems such as npm, Maven Central and crates.io. It will produce documented requirements, classification rules, a low-fidelity prototype and a structured performance evaluation. It does not aim to provide a production-ready package security scanner during this feasibility phase.

## Evidence-based verdicts

Each proposed check will return one of four verdicts, with supporting evidence and an explanation:

| Verdict | Meaning |
| --- | --- |
| **Agree** | Available evidence supports the declared value. |
| **Missing** | No usable value is declared. |
| **Conflict** | Credible evidence contradicts the declared value. |
| **Unverifiable** | Available evidence is insufficient for a reliable conclusion. |

A missing or inconsistent metadata field is **not, by itself, evidence of malicious behaviour**. NEXORYN will not label packages or maintainers as suspicious.

## Proposed anomaly categories

| ID | Category |
| --- | --- |
| **A1** | Missing licence information |
| **A2** | Licence inconsistency |
| **A3** | Missing repository information |
| **A4** | Invalid or inconsistent repository information |
| **A5** | Inconclusive metadata evidence |

## Planned six-month outputs

1. **Requirements and feasibility:** Review metadata standards and tools, define evidence sources and assess representative package releases.
2. **Rules and low-fidelity prototype:** Specify transparent verification and classification rules, registry mappings, interface mock-ups and sample CSV/JSON schemas.
3. **Performance evaluation:** Screen approximately 50 PyPI releases, conduct independent assessments of approximately 20, examine around 10 anomaly scenarios and document consistency, evidence completeness and limitations.
4. **Technical documentation:** Produce an automation roadmap and final feasibility report, with reusable technical outputs made publicly available where appropriate.

## Get involved

Feedback is welcome from SBOM and compliance-tool developers, open metadata curators and package maintainers. Once the project repository and contact channel are available, contributors will be able to raise issues and comment on the proposed rules.

The project plans to notify relevant maintainers of a **Conflict** verdict concerning their package at least four weeks before public disclosure, where contact details are available. Findings will be presented with their evidence and limitations.

## Licensing

The intended licences for outputs produced by the project are:

- **Rules, schemas and code:** Apache License 2.0.
- **Documents and project-generated data:** Creative Commons Attribution 4.0 (CC BY 4.0), subject to third-party rights and data-source terms.

## Project organisation

**NEXORYN** is proposed by **NEXT AI FUSION LIMITED**, Chelmsford, United Kingdom.

*This page describes a proposal, not an operational or completed service. Scope, deliverables and publication arrangements remain subject to funding and project planning.*

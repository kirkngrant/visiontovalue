# AI & Automation — Agent Opportunity Assessment

Status: design pilot, no autonomous agent deployed. Date: 2026-10-16.

## Decision principle
Start with a verified business-performance gap, not with AI availability. Assess data quality, deterministic alternatives, decision ownership, governance and measurable net benefit.

## Five-part scoring (0–2 each; total 10)
1. Material business gap
2. Data readiness and permission
3. Incremental AI advantage over Excel/BI/rules
4. Governance and human accountability
5. Measurable net benefit after operating cost and risk

## Candidate agent A — Performance exception analyst
Inputs: permissioned, anonymized contractual SLA measures and definitions.
Actions: validate schema, identify anomalies, suggest explanatory slices, draft executive narrative, create evidence links.
Boundaries: no unreviewed vendor claims; no changes to contracts, tickets, source data or external communication.
Human approval: all findings, explanations and remediation recommendations.
Baseline: Excel pivot tables, Power BI, SQL and threshold rules.
Success measures: analyst hours saved, false positive rate, issue-to-decision latency, adoption of corrective actions and realized SLA improvements.
Stop conditions: data leakage, weak source traceability, material hallucination or insufficient net benefit.

## Candidate agent B — Portfolio risk assistant
Use schedule and dependency data to flag emerging risk; compare against deterministic critical-path and earned-value reporting; humans own decisions.

## Candidate agent C — Career experience radiation assistant
Transform a reviewed canonical career story into resume variants, STAR stories, outreach and draft posts. Human verifies facts and authorizes publishing. No automatic applications or public posts.

## Pilot workflow
Intake -> gap analysis -> baseline -> data permission -> agent vs non-AI comparison -> small offline test -> governance review -> benefit validation -> deployment decision.

## Backlog
- [ ] Define one SLA anomaly test dataset using synthetic records.
- [ ] Create data dictionary and performance definitions.
- [ ] Prototype deterministic baseline before any LLM.
- [ ] Design traceable agent outputs and human review.
- [ ] Estimate operating costs and benefits.
- [ ] Record go/no-go decision and responsible owner.

No Shire confidential data or personal resume data is included in this public design note.

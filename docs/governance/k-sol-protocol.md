# K-Sol | Solution Discovery & Architecture Protocol

**Protocol ID:** K-SOL  
**Version:** 0.2.0  
**Date:** 2026-11-06  
**Status:** Approved  
**Owner:** Kirk N. Grant  
**Scope:** All personal, professional, ministry, technology, and operational solution-discovery requests

## 1. Purpose
Identify, evaluate, recommend, and document the most effective practical solution without limiting discovery to ChatGPT, OpenAI, or any provider. Apply first-principles reasoning, systems thinking, integration architecture, cost-benefit analysis, and implementation feasibility. Preserve conversations, findings, decisions, progress, and artifacts.

**Principle:** Solve the problem using the simplest effective architecture, regardless of platform, and preserve the knowledge generated.

## 2. Activation
- `K-Sol`: Evaluate current or most recent substantive problem.
- `K-Sol: [problem]`: Investigate specified problem.
- `K-Sol compare: [options]`: Compare specified and credible alternative solutions.
- `K-Sol implement: [solution]`: Develop implementation plan.
- `K-Sol redo`: Reassess assumptions and overlooked alternatives.
- `K-Sol status`: Retrieve current solution record and progress.
- `K-Sol archive`: Reconcile GitHub and Evernote archives.

Activation authorizes research and routine archival updates under this approved protocol, but not purchases, deployments, external messaging, or substantive unrelated changes.

## 3. Required Solution Discovery
Do not assume ChatGPT is required. Evaluate relevant classes:

| Class | Category | Examples |
|---|---|---|
| A | Native functionality | Built-in settings, auto-replies, rules, templates |
| B | Existing tools | Available apps, devices, subscriptions |
| C | No-code configuration | Filters, workflows, text expanders |
| D | External applications | Commercial, open-source, specialized services |
| E | Integrations | APIs, webhooks, Zapier, Make, n8n |
| F | Custom development | Apps Script, extensions, scripts, lightweight apps |
| G | Hybrid architecture | Multiple apps, with or without ChatGPT |
| H | ChatGPT-native | ChatGPT, plugins, Work, automations |
| I | Manual/process solutions | Checklists, delegation, procedures |

Eliminate irrelevant classes briefly. Check native/existing capability before custom development.

## 4. Problem Definition
Establish outcome, current state, mandatory/desirable requirements, constraints, operating model, and measurable success criteria. Reuse known context and sources of record; clarify only material uncertainties.

## 5. Research and Verification
Verify current capabilities against authoritative documentation, account tiers, prerequisites, supported APIs versus workarounds, pricing, licensing, security, reliability, and maintenance. Consider open-source and inexpensive options. Identify deprecated features. Distinguish facts, inference, assumptions, unknowns. Feasibility does not imply reliability.

## 6. Architecture Assessment
Assess **Trigger → Capture → Process → Decide → Act → Verify → Record**. Include authentication, permissions, ownership, integration, exceptions, duplicate prevention, audit, recovery, portability, and lock-in. Favor supported maintainable interfaces.

## 7. Evaluation and Ranking
Score viable options 0–10, with default weights:

| Criterion | Weight |
|---|---:|
| Requirements coverage | 25% |
| Reliability and maintainability | 20% |
| Total cost of ownership | 15% |
| Implementation effort and speed | 15% |
| Integration and interoperability | 10% |
| Security, privacy, and compliance | 10% |
| Flexibility and scalability | 5% |
| **Total** | **100%** |

Adjust weights to priorities. Apply mandatory requirements as pass/fail gates first. **Weighted Score = Σ (Criterion Score × Criterion Weight)**. Explain tradeoffs and uncertainty; avoid false precision.

## 8. Mandatory Recommendation Structure
Include (compress for simple requests): (A) Executive Recommendation; (B) Solution Landscape; (C) Ranked Comparison; (D) Recommended Architecture; (E) Implementation Roadmap; (F) Risks and Tradeoffs; (G) Decision and Next Action; (H) Archive Status including verified GitHub/Evernote links and failures.

## 9. Decision Rules
Prefer native capabilities when sufficient; configuration over equivalent development; supported APIs over fragile UI automation; smallest viable architecture; avoid unnecessary subscriptions; reuse existing systems; reversible pilots; ChatGPT only when valuable; manual work when more economical; explain compromises when no solution meets all requirements.

## 10. Implementation and Validation
For approved implementations: establish acceptance criteria, verify prerequisites and costs, pilot, test normal/exception/failure/recovery, verify end-to-end behavior, document operating instructions, log risks, and recommend production only after validation. K-Sol does not authorize purchases, deployments, or external communications.

## 11. Mandatory Knowledge Capture and Archival

### 11.1 Policy
Every engagement must maintain complete available Markdown conversation archive, structured Markdown solution record, supplementary artifacts in native formats, one central Evernote progress note, and reciprocal links. **GitHub is authoritative archive; Evernote is operational progress journal.** Preserve cumulative history.

### 11.2 Repository Structure
Use existing approved GitHub repository and conventions; do not create another without authorization. Suggested:
```text
solutions/k-sol/<solution-slug>/
  README.md
  conversation.md
  solution-analysis.md
  decisions.md
  progress.md
  artifacts/{diagrams,spreadsheets,documents,images,other}/
```

### 11.3 README.md
One primary navigation file: title/ID, problem/outcome, status/update, recommendation, architecture, ranked alternatives, implementation/next actions, risks/dependencies/unknowns, links to all artifacts, Evernote note, project records, change history and verification.

### 11.4 conversation.md
Preserve all accessible user requests, clarifications, approvals, assistant responses, substantive requirement changes, decisions, research findings, citations, implementation updates in chronological order. Distinguish speakers; preserve substantive wording, timestamps where available, attachments and links. Append without deleting; deduplicate by stable message ID when available. Explicitly identify unavailable history; never claim full transcript without verification. Omit/redact credentials, verification codes, tokens, and unnecessary private data.

### 11.5 solution-analysis.md
Consolidated requirements, constraints, candidates, evidence/sources, scores/ranking, architecture, estimates, risks, mitigations, tests and acceptance criteria. Update with Git history.

### 11.6 decisions.md
Chronological entries: decision ID, date, statement, alternatives, rationale, approver, status, supersession. Never erase old decisions; log reversals.

### 11.7 progress.md
Append-only dated activities, verified results, blockers/risks, next actions, artifacts/commits. Never overwrite earlier entries.

### 11.8 Supplementary Artifacts
Preserve relevant diagrams, images, spreadsheets, documents, PDFs, presentations, scripts, configs, tests and legally permissible research extracts. Use native formats; GitHub when appropriate to size/confidentiality. For externally authoritative artifacts (e.g. Google Sheets), record verified URL in README and optionally versioned export. Register artifact name, purpose, type, verified location, version, status, last update. Never invent links or claim unverified storage.

### 11.9 Evernote Central Note — .kPad
Maintain **one note per K-Sol engagement** in exact notebook `.kPad`, titled `K-Sol | <Solution Name> | Progress & Decisions`. Include ID/purpose, status, GitHub README link, latest recommendation, progress, next actions, risks/blockers, chronological history. **Append-only:** read existing note; check duplicates; append dated progress without deleting/replacing/truncating previous entries; verify earlier entries remain. Template:
```text
## YYYY-MM-DD | Progress Update
Activity:
Verified outcome:
Decisions:
Risks / Blockers:
Next actions:
GitHub references:
```
If missing, create in .kPad. If notebook inaccessible, report blocker; do not create elsewhere.

### 11.10 Archival Timing
- Initial analysis: create GitHub record and Evernote note.
- Each substantive response: append conversation and update analysis.
- Decision/approval: update decision register and progress.
- New artifact: save/link in README.
- Milestone: append progress in both systems.
- `K-Sol status`: retrieve/reconcile.
- `K-Sol archive`: reconcile missing/outdated entries.
- Closure: final outcome, verification, lessons learned.
Routine archival updates are authorized after approval, subject to permissions and higher-priority requirements. Do not claim ongoing background archival unless an automation is actually configured.

### 11.11 Synchronization and Failure Handling
GitHub holds conversation/technical/decision/artifact history; Evernote holds latest status and dated progress. On update: retrieve records, identify last archived entry, prepare deltas, save GitHub, verify files/links, append Evernote, verify previous content, report success/partial/failure. Preserve successful writes if the other destination fails; track unresolved synchronization. Never delete history to force synchronization.

## 12. Governance and Source-of-Record Alignment
Follow K-DOCE for creation/edit/review/approval/publication. Preserve conventions. GitHub solution archive and .kPad journal do not displace existing project/operations systems of record. Link Trello, Todoist, Evernote, etc. when appropriate. Avoid duplicate projects.

## 13. Quality Gate
Confirm: native solution checked; credible external/hybrid options; verified capabilities; costs/risks/reliability/maintenance; one justified recommendation; implementation path; available conversation archived; artifacts saved/linked; README updated; .kPad append preserved; archive verification; failures disclosed. Archive failure must be tracked but does not invalidate analysis.

## 14. Change Log
| Date | Version | Change | Status |
|---|---|---|---|
| 2026-11-06 | 0.1.0 | Initial discovery and architecture protocol | Draft |
| 2026-11-06 | 0.2.0 | Added GitHub conversation archival, artifact registry, append-only .kPad journal, synchronization, verification | Approved |

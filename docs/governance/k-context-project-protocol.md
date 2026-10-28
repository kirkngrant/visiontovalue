# K-CONTEXT | Project-Level Context Lifecycle Protocol

Version: 1.0  
Date: 2026-10-28  
Status: Proposed for installation in ChatGPT Project Instructions  
Scope: 00 | DASHBOARD project; other projects only if separately installed.

## Purpose
Capture durable decisions and state from long ChatGPT conversations, archive transaction-specific detail, and resume from a versioned GitHub checkpoint. This is a **logical** checkpoint, not deletion of chat history or forced clearing of a model context window.

## Command syntax
All commands use a dash flag, never a colon.

| Command | Intent |
| --- | --- |
| `savec` | Save durable context from current chat |
| `savec -topic [topic]` | Save named topic/thread |
| `savec -all` | Save identifiable active topics separately |
| `savec -checkpoint` | Save current state and establish a logical resume anchor |
| `savec -close` | Archive a completed transaction; retain final outcomes and lessons |
| `savec -reload [topic]` | Retrieve most recent saved topic from canonical source |
| `savec -diff [topic]` | Compare saved baseline with current discussion |
| `savec -resume [topic]` | Reload and continue from outstanding next actions |

## Classes
- **PERSISTENT:** stable preferences, operating standards and recurring constraints.
- **PROJECT:** scope, decisions, work products, status, RAID, dependencies and next actions.
- **TRANSACTION:** short-lived activity; retain final result and verification, archive intermediate detail.
- **TEMPORARY:** exploration, debugging and scratch work; omit unless needed for reproducibility.
- **SUPERSEDED:** prior state no longer authoritative; preserve version history but exclude from current baseline.

## Save workflow
1. Identify requested scope, current chat information and any existing authoritative context.
2. Distinguish **verified fact**, **user decision**, **proposal**, **assumption**, **open question**.
3. Minimize sensitive content; never publish credentials, tokens, private financial/health information or unnecessary identifying data.
4. Draft human-readable Markdown and structured JSON with matching `topic_id`, `checkpoint_id`, `version`, `saved_at`, `status`, `source_scope`, `decisions`, `constraints`, `artifacts`, `open_actions`, `risks`, `superseded`, and `resume_prompt`.
5. If an authorized **private** context repository exists and GitHub access is available, publish/update both files; use unique checkpoint IDs, compare existing versions, and avoid overwriting unrelated content.
6. Read back both files and verify IDs, version and expected content; only then report success.
7. Return verified URLs, commit SHA, summary, open actions and a ready-to-use `savec -resume [topic]` instruction.
8. If no private repo or access exists, create local portable Markdown/JSON artifacts when available, and clearly state that GitHub publishing was not performed.
9. For `-close`, preserve final outcome, decision rationale, artifact IDs, verified URLs, outstanding follow-up and lessons; do not delete source chat or Git history.
10. For `-reload` and `-resume`, retrieve latest checkpoint, show provenance, use it as preferred baseline, and identify any conflict with newer explicit user instructions. Never claim to physically purge earlier messages.

## Storage layout (private repository recommended)
```text
kgrant-context/
  README.md
  config/context-policy.json
  persistent/
  projects/<topic>/current.md
  projects/<topic>/current.json
  projects/<topic>/history/
  transactions/active/
  transactions/closed/
  checkpoints/checkpoint-index.json
```

## Scope and limitations
- Commands are **conversational conventions**, not built-in ChatGPT commands.
- Project Instructions must be installed manually in ChatGPT for reliable project-wide recognition; a GitHub document alone does not install them.
- A GitHub connector is needed for publishing and readback. Context from other chats may not be fully accessible; do not invent missing context.
- No selective message purge, context-window reset or automatic deletion is available from prompts.
- A fresh chat + `savec -resume [topic]` is the cleanest practical reset.
- K-DOC formal registration is optional for individual context checkpoints unless requested.

## Suggested project-instruction block
```text
K-CONTEXT protocol: Interpret savec, savec -topic [name], savec -all, savec -checkpoint,
savec -close, savec -reload [topic], savec -diff [topic], and savec -resume [topic]
according to the K-CONTEXT protocol at
https://github.com/kirkngrant/visiontovalue/blob/main/docs/governance/k-context-project-protocol.md.
Use dash flags only. Classify context as PERSISTENT, PROJECT, TRANSACTION,
TEMPORARY or SUPERSEDED. Save durable outcomes, decisions, links and open work;
summarize disposable intermediate details. For GitHub writes, use an authorized
private context repository, never publish sensitive chat context to a public repo.
Verify writes by readback. If source data or GitHub access is unavailable, disclose
that limitation. Checkpoints are logical only; never claim to erase chat messages.
For a clean context restart, recommend a new chat with savec -resume [topic].
```

## Change log
- 2026-10-28 v1.0: Defined dash-only command grammar and project installation protocol.

# CORTEZIA — CODEX MICRO-PACK WORKFLOW

Status: ACTIVE / EXPLICIT DECISION — 2026-09-03

## Core roles
- Continuity assistant = memory, canon, Drive + GitHub sync, target analysis, asset selection, micro-pack preparation.
- Codex = targeted local executor.

## Unit of work
ONE SCREEN = ONE MICRO-PACK.

Typical pack:
```
CORTEZIA_SCREEN_XX/
├── PROMPT.txt
├── TARGET.png
├── SCREEN.json
├── BRAND/
└── ASSETS/
```
Include only what the screen actually needs.

## Codex hard rules
DO NOT AUDIT THE WHOLE REPOSITORY.
DO NOT READ OLD REPORTS.
DO NOT SEARCH DRIVE.
DO NOT SEARCH GITHUB.
DO NOT REOPEN PREVIOUS VISUAL PACKS.
Do not scan unrelated routes/components.

Read only:
1. PROMPT.txt
2. SCREEN.json
3. TARGET.png
4. assets explicitly listed in SCREEN.json
5. existing runtime files directly required for this screen

Preserve current Cortezia architecture.
No commit/push/deploy unless explicitly authorized for the website repository.

## Reuse learned paths
Maintain `CODEX/CORTEZIA_CODEX_MAP.json`.
Once a runtime path has been established by Codex, future screen missions reuse it instead of rediscovering it, unless the worktree materially changed or the path becomes stale.

## Target interpretation
TARGET.png is a GOLDEN VISUAL TARGET only.
Never use it as a clickable screenshot, background implementation or hotspot map.
Use structural art + real runtime DOM/SVG/HTML/CSS/JS.

## Targeted validation during screen work
Prefer:
- targeted TypeScript/typecheck when possible;
- lint changed files;
- functional tests for the affected behavior;
- render target route/state;
- screenshot;
- compare/fix/recapture.

Do NOT automatically run:
- every project test;
- full production build;
- full security audit;
- every Playwright route.
Run global validation after a significant group of screens or before a global/final validation.

Sensitive screens such as Age Gate keep their relevant security/functional tests.

## Output mode
OUTPUT_MODE=MINIMAL

Do not narrate exploration.
Do not explain routine commands.
Do not repeat the specification.
Do not summarize supplied files.

Final response only:
- STATUS
- FILES_CHANGED
- TESTS
- CAPTURE
- VISUAL_GAPS
- SNAPSHOT

## Workflow
USER → target/corrections → continuity assistant → canonical storage → micro-pack → Codex local targeted execution → render/capture → targeted repair/tests → STOP.

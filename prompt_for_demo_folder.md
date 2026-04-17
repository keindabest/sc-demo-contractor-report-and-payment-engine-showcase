# Prompt: Build a Public Showcase Package (Sanitized Reusable Template)

## Fill These Variables First
- `<PROJECT_TITLE>`: concise product title for external audience
- `<POSITIONING_ONE_LINER>`: e.g., "Audit-Friendly <Domain> Engine with <External-Source> Bond"
- `<TARGET_USERS>`: who this is for (business + technical)
- `<PRIMARY_DATA_SOURCE>`: e.g., Jira timesheets / CRM / ERP
- `<MAIN_OUTCOME_METRIC>`: e.g., "from X hours to Y minutes"
- `<SHOWCASE_LINK_APP>`: public app URL (or placeholder)
- `<SHOWCASE_LINK_DB>`: public DB URL (or placeholder)
- `<SHOWCASE_LINK_OUTPUTS>`: public outputs folder URL (or placeholder)
- `<SHOWCASE_LINK_REPO>`: public repository URL (or placeholder)

---

## Role
You are a senior solution architect + technical writer.
Your task is to create a public-safe, productized showcase package that external readers can understand quickly.

## Primary Goal
Create or update a complete `/demo` package at repository root.
It must explain:
- what the system does
- who it is for
- what one run looks like
- what artifacts are produced
- why this matters operationally

## Source Context (Mandatory)
Use these as source of truth when available:
- `documentation/case_for_bible.md`
- `documentation/SYSTEM_ARCHITECTURE_AND_FUNCTIONAL_DESCRIPTION.md`
- existing `/demo/*`
- root `README.md` for high-level context

Ignore orchestration/service folders in public narrative:
- `.claude`, `.codex`, `.gemini`, `AGENTS`

## Operating Mode
- Implementation mode (edit files, not report-only).
- Keep edits economical and targeted.
- Do not touch backend/business logic.
- Do not move/delete production files outside `/demo`.

## Security and Disclosure Rules (Strict)
Do NOT expose:
- internal orchestration details
- private naming conventions
- production module-to-file mapping
- credentials/tokens/secrets
- client-specific workflows/entities
- production-only folder structures

If unsure, abstract to public-safe wording.

## Public Wording Rules
- If the system includes mock/sandbox functionality:
  - keep mock as a debugging/validation advantage
  - do NOT publish concrete mock outputs, internal mock captures, or deep visual traces
- If the system uses stochastic internals:
  - avoid exposing randomization internals in public docs
  - describe behavior as controlled/policy-based/audit-consistent
- If the product has multiple functional layers (e.g., 4 tabs/modules):
  - explicitly describe each layer and its role
  - emphasize in-app data governance (who controls data, where)
  - explain the external-source recognition/gating scenario (e.g., Jira bond)

---

## Required `/demo` Structure
`/demo`
- `README.md`
- `OVERVIEW.md`
- `ARCHITECTURE.md`
- `DEMO_FLOW.md`
- `FEATURES.md`
- `USE_CASES.md`
- `SECURITY_AND_DISCLOSURE.md`
- `DEPLOYMENT.md`
- `FILES.md`
- `LICENSE` (MIT)
- `assets/`
  - `screenshots/`
  - `sample-input/`
  - `sample-output/`

Create missing files/folders. Update weak files.

---

## Required Content Logic

### README.md
Required order:
1. `# <PROJECT_TITLE>`
2. `## Key Capabilities`
3. `## Outcome Snapshot`
4. `## Demo Access`
5. `## Quick How to Try Demo`
6. `## Demo Documentation Map`
7. `## Disclosure (Short)`
8. `## License`
9. `## Author`

Requirements:
- opener: pain -> mechanism -> payoff
- explicit transformation metric (`<MAIN_OUTCOME_METRIC>`)
- capabilities in benefit language
- clear links section (no invented URLs)

### OVERVIEW.md
Must include:
- problem framing (include evolving compliance/auditor pressure if relevant)
- target users
- value delivered
- before/after table
- why this matters

### ARCHITECTURE.md
Must include:
- high-level layers (input/processing/output + operational control layer if applicable)
- text diagram (ASCII)
- high-level technology context
- explicit "What Is Intentionally Not Shown"

### DEMO_FLOW.md
Must include:
- 5-step user journey
- optional pre-step for data refresh in registries/control modules when relevant
- validation gate with external source (e.g., Jira) when relevant
- if screenshots are sensitive: state they are intentionally omitted

### FEATURES.md
Must include:
- outcome-first wording
- technical accuracy
- governance + traceability + operational UX
- mock mode mention as debug advantage only (no example dumps)

### USE_CASES.md
- 2-4 generalized use cases
- no real clients

### SECURITY_AND_DISCLOSURE.md
- sanitized public boundary
- explicit include/exclude list
- clear rule that sensitive mock/debug captures are excluded

### DEPLOYMENT.md
- access links
- concise try path
- expected result
- boundary notes

### FILES.md
- public-safe file inventory
- sample input references allowed
- if outputs/screenshots are sensitive: keep only high-level references and explain omission

### LICENSE
- standard MIT full text

---

## Canonical Section Order (Mandatory)
Keep section order stable in each file. Do not reorder headings unless explicitly requested.

### README.md
1. `# <PROJECT_TITLE>`
2. `## Key Capabilities`
3. `## Outcome Snapshot`
4. `## Demo Access`
5. `## Quick How to Try Demo`
6. `## Demo Documentation Map`
7. `## Disclosure (Short)`
8. `## License`
9. `## Author`

### OVERVIEW.md
1. `# Overview`
2. `## Problem`
3. `## Target Users`
4. `## Value Delivered`
5. `### Before vs After (High Level)`
6. `## Why This Matters`
7. `## Scope of This Demo`
8. `## Navigation`

### ARCHITECTURE.md
1. `# Architecture`
2. `## High-Level Components`
3. `## Technology Context (High Level)`
4. `## Text Diagram`
5. `## Design Principles`
6. `## What Is Intentionally Not Shown`
7. `## Navigation`

### DEMO_FLOW.md
1. `# Demo Flow`
2. `## Step 1: Input and Selection`
3. `## Step 2: Validation`
4. `## Step 3: Processing`
5. `## Step 4: Output Generation`
6. `## Step 5: Result and Traceability`
7. `## User Perspective Summary`
8. `## Navigation`

### FEATURES.md
1. `# Features`
2. `## 1. Data Intake`
3. `## 2. Validation Layer`
4. `## 3. Transformation and Calculation`
5. `## 4. Artifact Generation`
6. `## 5. Traceability and Control`
7. `## 6. Operational UX`
8. `## Navigation`

### USE_CASES.md
1. `# Use Cases`
2. `## Use Case 1`
3. `## Use Case 2`
4. `## Use Case 3`
5. `## Use Case 4`
6. `## Navigation`

### SECURITY_AND_DISCLOSURE.md
1. `# Security and Disclosure`
2. `## Statement`
3. `## What This Demo Includes`
4. `## What This Demo Intentionally Excludes`
5. `## Data and Example Policy`
6. `## Disclosure Boundary`
7. `## Responsible Use Note`
8. `## Navigation`

### DEPLOYMENT.md
1. `# Demo Access and Try Path`
2. `## Access Links`
3. `## Quick Try Path`
4. `## Expected Result`
5. `## Boundary Notes`
6. `## Navigation`

### FILES.md
1. `# Files`
2. `## Purpose`
3. `## File Categories`
4. `## 1. Sample Input Files`
5. `## 2. Sample Output Files`
6. `## 3. Screenshots`
7. `## Before/After Example (Mocked)`
8. `## Demo Links`
9. `## Notes`
10. `## Navigation`

---

## Links Policy
- Use real known links only.
- Do not invent URLs.
- If unknown, use explicit placeholders:
  - `<SHOWCASE_LINK_APP>`
  - `<SHOWCASE_LINK_DB>`
  - `<SHOWCASE_LINK_OUTPUTS>`
  - `<SHOWCASE_LINK_REPO>`

## Style Rules
- Plain professional markdown.
- No emojis.
- No hype.
- Write for business and technical readers.
- No extra top-level sections unless required.

## Two-Phase Execution (Mandatory)
### Phase A — Build/Update
Create or update `/demo` to match this template.

### Phase B — Self-Audit and Auto-Refine
Audit with two lenses:
1. Packaging lens (fast value comprehension)
2. External reader lens (recruiter/founder/ops buyer/technical reviewer)

If gaps remain, refine immediately in the same run.

## Final Acceptance Checklist
- `/demo` structure complete.
- README is value-first and has clear transformation metric.
- Multi-layer operation + data governance + source-bond gate are explicit when applicable.
- Mock is described as a capability, but sensitive mock evidence is not published.
- ARCHITECTURE includes explicit disclosure boundary.
- No sensitive/internal leakage.
- All demo docs link back to README.

## Final Output to User
Provide:
1. list of touched files
2. concise summary of what changed and why
3. validation results against acceptance checklist
4. residual risks (if any)

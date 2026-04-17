# Architecture

## High-Level Components
- Operational Control Layer (4 Tabs): Generation, Contractor Registry, Customer Registry, and Role Configuration.
- Input Layer: operator form, contractor/customer/period selection, and sync initiation.
- Processing Layer: snapshot assembly, policy-based allocation calculation, and concurrency control.
- Output Layer: document generation, PDF outputs, and Drive folder provisioning with archive behavior.

## Technology Context (High Level)
The demo reflects a Google Workspace stack centered on Apps Script, Google Sheets, Google Docs, and Google Drive, with a browser UI and PDF post-processing.

## Text Diagram
```text
[ Operator UI ]
  |-- Generation Tab
  |-- Contractor Registry Tab
  |-- Customer Registry Tab
  |-- Role Configuration Tab
      |
      v
[ Validation + Sync Gate ]
      |
      v
[ Snapshot Builder ]  (input + registry + config context)
      |
      v
[ Allocation + Checksum Control ]
      |
      v
[ Document Generation Pipeline ]
  |        |          |
  v        v          v
[Docs]   [Sheets]   [PDF Outputs]
      \      |      /
       \     |     /
        v    v    v
      [ Drive Folder Provisioning + Archive ]
                |
                v
        [ Traceability Links ]
```

## Design Principles
- Defensive compliance posture: the workflow is designed for predictable evidence production.
- Snapshot-based execution: each run is anchored to a captured context state.
- Controlled calculations: monetary decomposition stays cent-consistent via checksum rules.
- In-app governance: database records and Jira recognition scenario are managed in the same operational console.
- Operator clarity: each stage is explicit and verifiable in sequence.

## What Is Intentionally Not Shown
- Internal orchestration scripts and private naming conventions.
- Production-only IDs, secret configuration, or credential material.
- Client-specific entities and private workflow mappings.
- Any implementation details that could imply private environment access.

## Navigation
- [README](README.md)
- [Overview](OVERVIEW.md)
- [Demo Flow](DEMO_FLOW.md)
- [Features](FEATURES.md)
- [Use Cases](USE_CASES.md)
- [Security and Disclosure](SECURITY_AND_DISCLOSURE.md)
- [Demo Access and Try Path](DEPLOYMENT.md)
- [Files](FILES.md)

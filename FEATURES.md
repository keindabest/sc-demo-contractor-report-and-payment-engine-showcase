# Features

## 1. Data Intake
The Generation tab captures contractor, customer, and billing period inputs in one place to reduce handoff friction.

## 2. Validation Layer
Generation remains gated until context sync and Jira recognition checks complete, preventing partial or ambiguous runs.

## 3. Transformation and Calculation
The system transforms validated inputs into service-line outputs using policy-based calculation rules with cent-level checksum consistency, informed by role and registry data managed in-app.

## 4. Artifact Generation
Template-driven document outputs are assembled and exported in a reproducible structure suitable for operational review.

## 5. Traceability and Control
Each run leaves a navigable evidence path from source context to generated files, with archive-first handling for prior artifacts and direct linkage back to managed database records.

## 6. Operational UX
The experience is optimized for recurring operations through four coordinated tabs: Generation, Contractor Registry, Customer Registry, and Role Configuration. Teams can fully manage database content and Jira recognition behavior from the same application surface. Mock mode is kept as a debugging advantage, while mock captures are excluded from the public package.

## Navigation
- [README](README.md)
- [Overview](OVERVIEW.md)
- [Architecture](ARCHITECTURE.md)
- [Demo Flow](DEMO_FLOW.md)
- [Use Cases](USE_CASES.md)
- [Security and Disclosure](SECURITY_AND_DISCLOSURE.md)
- [Demo Access and Try Path](DEPLOYMENT.md)
- [Files](FILES.md)

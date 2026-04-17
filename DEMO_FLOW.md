# Demo Flow

## Step 1: Input and Selection
The operator opens the application and verifies required data in the four-tab control center (Generation, Contractor Registry, Customer Registry, Role Configuration).

Optional Step 1A: Data Refresh in Registries
- If the people list or linked customer/role records are outdated, the operator updates data directly in the registry tabs before generation.
- This keeps contractor/customer selections and related billing context current for the run.

After optional updates, the operator selects contractor/customer/month/year in the Generation tab.

Public note: screenshots and explicit mock result captures are intentionally omitted from this package.

## Step 2: Validation
The operator runs the sync stage. The system validates context completeness and the configured Jira recognition scenario, keeping generation controls locked until the validation gate passes.

## Step 3: Processing
After validation, the system captures a run snapshot, applies policy-based allocation checks, and prepares output targets with concurrency protection using current in-app database state.

Optional debug path: operators can run mock-mode checks for scenario validation before live generation, without publishing internal mock captures.

## Step 4: Output Generation
The pipeline generates the required billing artifacts, applies template mappings, and produces final output files with structured naming.

## Step 5: Result and Traceability
Generated files are placed in a target Drive folder, and the input record points to that folder for direct evidence lookup.

## User Perspective Summary
From the operator perspective, the flow is linear: maintain data in the control tabs, select context, validate, generate, and review outputs. The process emphasizes control and repeatability over manual document assembly. Results are immediately discoverable through linked storage artifacts.

## Navigation
- [README](README.md)
- [Overview](OVERVIEW.md)
- [Architecture](ARCHITECTURE.md)
- [Features](FEATURES.md)
- [Use Cases](USE_CASES.md)
- [Security and Disclosure](SECURITY_AND_DISCLOSURE.md)
- [Demo Access and Try Path](DEPLOYMENT.md)
- [Files](FILES.md)

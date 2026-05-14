---
description: Create or update the project constitution with aviation compliance laws (FAA, DOT, PII, audit trail).
---

## User Input

```text
$ARGUMENTS
```

## Outline

1. Create or update the project constitution and store it in `.specify/memory/constitution.md`.
   - Pre-loaded with aviation compliance principles:
     - **ENG-4.1** — Atomic TDD (RED → GREEN → REFACTOR → VERIFY → COMMIT)
     - **ENG-4.2** — Test Pyramid (unit > integration > E2E)
     - **ENG-3.1** — Complexity Limits (test files < 300 LOC, page objects < 200 LOC)
     - **ENG-6.1** — Security by Design (no hardcoded credentials, auth state gitignored)
     - **ENG-6.4** — Data Encryption (PII encrypted at rest and in transit, never logged raw)
     - **ENG-6.7** — Audit Trail (every operation logged with correlation ID)
     - **BUS-2.1** — FAA Compliance (aviation safety for device/station operations)
     - **BUS-2.3** — DOT Consumer Protection (passenger rights for messaging features)
   - Derive project-specific details from user input and existing repo context (README, docs)
   - Fill `[PROJECT_NAME]`, `[RATIFICATION_DATE]`, and `[LAST_AMENDED_DATE]` placeholders

2. If the user provides additional principles, append them after the existing aviation laws.

3. Validate that no prohibited actions from the template are contradicted by user input.

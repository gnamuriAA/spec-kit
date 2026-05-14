# [PROJECT_NAME] Constitution

## Core Principles

### I. Atomic TDD (ENG-4.1) — NON-NEGOTIABLE
Every code change follows the RED → GREEN → REFACTOR → VERIFY → COMMIT cycle. Only one test is written per TDD cycle. No code is merged without a passing test that exercises the change.

### II. Test Pyramid (ENG-4.2)
Testing follows the pyramid structure: many unit tests at the base, fewer integration tests in the middle, and the fewest E2E tests at the top. Unit tests are the fastest and cheapest layer. E2E tests are reserved for critical user journeys that cannot be validated at lower levels.

### III. Complexity Limits (ENG-3.1)
No test file exceeds 300 lines of code. No page object exceeds 200 lines of code. Complexity must be justified and kept within measurable bounds.

### IV. Security by Design (ENG-6.1) — NON-NEGOTIABLE
Every feature includes security requirements before implementation begins. No credentials are hardcoded in source code or test files. Authentication state files are excluded from version control. Credentials are sourced exclusively from environment variables.

### V. Data Encryption & PII Protection (ENG-6.4) — NON-NEGOTIABLE
Personally identifiable information (PII) is encrypted at rest and in transit. Raw PII — including names, email addresses, payment card numbers, and passport numbers — must never appear in log output. PII handling is validated through dedicated unit tests.

### VI. Audit Trail (ENG-6.7) — NON-NEGOTIABLE
Every operation is logged with a correlation ID. All CRUD mutations include traceable variables in their payloads. Audit trail compliance is verified through unit tests on every service that performs mutations.

## Regulatory Compliance

### VII. FAA Compliance (BUS-2.1) — NON-NEGOTIABLE
Aviation safety requirements are applied to all device, station, and operational management features. Device provisioning, station assignment, and cron job region management are validated through tests. No operational feature ships without regression coverage.

### VIII. DOT Consumer Protection (BUS-2.3) — NON-NEGOTIABLE
Passenger rights and consumer protection requirements are enforced in all messaging and communication features. Message center operations — creation, scheduling, publishing, and delivery tracking — are validated through tests.

## Prohibited Actions

The following actions violate this constitution and must never occur:

| Prohibited Action | Law Violated |
|-------------------|-------------|
| Writing more than one test per TDD cycle | ENG-4.1 |
| Shipping code without security requirements | ENG-6.1 |
| Hardcoding credentials in source or test code | ENG-6.1 |
| Logging raw PII (names, PAN, passport numbers) | ENG-6.4 |
| Operations without correlation ID in log | ENG-6.7 |
| Skipping law citations in proposals | ENG-11.1 |
| Deploying untested device/station operations | BUS-2.1 |
| Deploying untested message center operations | BUS-2.3 |

## Governance

This constitution is the highest authority for all development in this project. It supersedes all other practices, preferences, and conventions. Amendments require documentation, stakeholder approval, and a migration plan for existing code.

All pull requests and code reviews must verify compliance with these principles. Every proposal must cite the applicable laws from this constitution.

**Version**: 1.0.0 | **Ratified**: [RATIFICATION_DATE] | **Last Amended**: [LAST_AMENDED_DATE]

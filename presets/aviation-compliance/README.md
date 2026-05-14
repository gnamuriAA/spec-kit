# Aviation Compliance Governance Preset

A [Spec Kit](https://github.com/github/spec-kit) preset that enforces aviation industry compliance laws for software development — covering FAA safety, DOT consumer protection, PII encryption, audit trails, and TDD practices.

## Laws Included

| Law | Name | Requirement |
|-----|------|-------------|
| **ENG-3.1** | Complexity Limits | Test files < 300 LOC; page objects < 200 LOC |
| **ENG-4.1** | Atomic TDD | RED → GREEN → REFACTOR → VERIFY → COMMIT per test |
| **ENG-4.2** | Test Pyramid | Many unit tests (base), fewer integration (middle), fewest E2E (top) |
| **ENG-6.1** | Security by Design | No hardcoded credentials; auth state gitignored |
| **ENG-6.4** | Data Encryption | PII encrypted at rest and in transit; never logged raw |
| **ENG-6.7** | Audit Trail | Every operation logged with correlation ID |
| **BUS-2.1** | FAA Compliance | Aviation safety requirements for device/station operations |
| **BUS-2.3** | DOT Consumer Protection | Passenger rights enforced for messaging features |

## Installation

```bash
specify preset add aviation-compliance
```

Or manually copy the preset folder to your `.specify/presets/` directory.

## Usage

After installing the preset, generate your project constitution:

```bash
specify constitution "My Aviation Admin App"
```

This creates `.specify/memory/constitution.md` pre-loaded with all aviation compliance principles.

## What It Provides

- **Constitution Template** — Pre-filled with 8 aviation compliance laws, prohibited actions table, and governance rules
- **Constitution Command** — Customized `speckit.constitution` command that guides you through setting up compliance

## Origin

These laws are derived from the **Hangar AI Constitution** used at American Airlines TechOps for internal productivity applications that manage airport devices, stations, and passenger-facing messaging systems.

## License

MIT

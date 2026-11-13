# T02 — Seeded mutation catch rate

Canonical public record: [https://migrateforge.com/proof/](https://migrateforge.com/proof/)

**Deterministic plant sites. Earlier, higher figures used randomised sites and are withdrawn.**

Seed key (engine image `86222b7`): `1:86222b7f2fc5386b2d18fdd3e41da06b54b6e89b`

Excluded rate = caught / (caught + missed) after dropping EQUIVALENT and operator NOT_APPLICABLE.

## Waves (record)

| Wave | Excluded rate | Caught / missed | Raw |
| --- | ---: | ---: | ---: |
| WA Blast Pro wave 1 | **57.14%** | 24/42 | 53.33% (24/45) |
| InvoicePlane wave 1 | **35.89%** | 14/39 | 33.33% (14/42) |

WA Blast Pro wave 2 has no seeded catch-rate record (parity verify remains 379/379).

## Five critical categories (seeded)

| Category | WA Blast Pro wave 1 | InvoicePlane wave 1 |
| --- | --- | --- |
| Lost writes (`SKIP_SIDE_EFFECT`) | 100% (3/3) | 100% (1/1) |
| Outgoing calls (`OUTBOUND_PAYLOAD`) | 100% (2/2) | not 100% — NOT_REACHED |
| Escaping (`MISSING_ESCAPE`) | not 100% (2/3) | not 100% (2/3) |
| HTTP status | 100% (3/3) | not 100% (2/3) |
| Access control (AUTH / CSRF / TENANT) | not 100% of reached (AUTH 0/3, CSRF 2/2, TENANT NOT_REACHED) | not 100% (AUTH 2/3, CSRF 0/3, TENANT 0/2) |

Source methodology: MigrateForge internal T02 harness notes; numbers match the published proof page.

# MigrateForge public benchmarks

Sanitized **100/100/100** parity scorecards for MigrateForge’s published PHP → Java 21 / Spring Boot migration benchmarks.

**Canonical public record:** [https://migrateforge.com/proof/](https://migrateforge.com/proof/)

| Suite | Role | Result |
| --- | --- | --- |
| **4 migrated waves** | WA Blast Pro waves 1–2 + InvoicePlane waves 1–2 | **858** verified journeys at **100/100/100** parity, write-effect diffs **0** |
| **Q07 CI3 conformance** | CodeIgniter 3 adapter suite (not an app migration wave) | **83/83** fixtures at **100/100/100** |

Both application suites are **benchmarks**, not client projects. WA Blast Pro is MigrateForge’s own production multi-tenant SaaS (source is **not** in this repo). InvoicePlane is open source: [InvoicePlane/InvoicePlane](https://github.com/InvoicePlane/InvoicePlane).

## Scorecards

| Scorecard | Matched fixtures | Coverage of capture |
| --- | ---: | ---: |
| [WA Blast Pro wave 1](scorecards/wa-blast-pro-wave-1.md) | 193/193 | 193/194 |
| [WA Blast Pro wave 2](scorecards/wa-blast-pro-wave-2.md) | 379/379 | 379/380 |
| [InvoicePlane wave 1](scorecards/invoiceplane-wave-1.md) | 133/133 | 134/138 |
| [InvoicePlane wave 2](scorecards/invoiceplane-wave-2.md) | 153/153 | 153/153 |
| [Q07 CI3 conformance](scorecards/ci3-conformance-q07.md) | 83/83 | — |
| [T02 seeded catch rate](scorecards/catch-rate-t02.md) | WABP1 **57.14%** (24/42); IP1 **35.89%** (14/39) | — |

Sum of the four application waves: **858** matched fixtures.

## What “100/100/100” means

On every compared recorded journey in the wave:

1. **Fixture parity** — HTTP responses match  
2. **De-duplicated parity** — distinct journeys match after de-duplication  
3. **Route-weighted parity** — match weighted by route coverage  

Plus **write-effect differences = 0** (database mutations and outbound API payloads).

Behaviour that was never recorded is outside the claim. See [methodology.md](methodology.md).

## Free size/risk reports (not parity)

These measure application size and risk for pricing. They are **not** parity results and contain **no** source code:

- [wa-blast-pro free report (PDF)](https://migrateforge.com/samples/wa-blast-pro.pdf)
- [InvoicePlane free report (PDF)](https://migrateforge.com/samples/invoiceplane.pdf)

## What this repo does **not** contain

- PHP or generated Java source for WA Blast Pro  
- Database dumps, traffic captures, or fixture payloads  
- Customer code or secrets  

## Product

[MigrateForge](https://migrateforge.com/) migrates PHP applications to Java Spring Boot and blocks cutover until recorded journeys match.

- Proof: https://migrateforge.com/proof/  
- How it works: https://migrateforge.com/how-it-works/  
- Contact: https://migrateforge.com/contact/

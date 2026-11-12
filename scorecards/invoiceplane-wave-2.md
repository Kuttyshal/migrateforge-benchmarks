# InvoicePlane — wave 2

Canonical public record: [https://migrateforge.com/proof/](https://migrateforge.com/proof/)

## Application

| Field | Value |
| --- | --- |
| Benchmark | [InvoicePlane](https://github.com/InvoicePlane/InvoicePlane) (public OSS) |
| Stack measured in free report | CodeIgniter 3.4.0 |
| Wave | 2 of the published migrated set |
| Scope (published) | 49 units, 1,667 lines of PHP across six CRUD modules |
| Source in this repo | **None** — use upstream InvoicePlane |

## Parity (SUCCEEDED)

| Measure | Result |
| --- | ---: |
| Fixture | **100%** |
| De-duplicated | **100%** |
| Route-weighted | **100%** |
| Matched fixtures | **153/153** |
| Coverage of capture | **153/153** |
| Write-effect differences | **0** |
| HIGH quality findings | **0** |
| Tests | 216 |

## Honest middle (before hand fixes)

| Milestone | Distinct-journey match |
| --- | ---: |
| First full 3D comparison after the generated app would start | **82%** |
| After hand fixes | **100%** |
| Hand-fix rate | **9.7** per 1,000 PHP lines |

Most fixes landed in the CodeIgniter adapter layer (redirect, validation messages, model pagination / form values), so the next CI3 application starts with them already solved.

## Free report (size / risk / price — not parity)

https://migrateforge.com/samples/invoiceplane.pdf

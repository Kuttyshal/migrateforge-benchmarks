# Methodology

Canonical narrative and numbers: [https://migrateforge.com/proof/](https://migrateforge.com/proof/)

## Recorded journeys

MigrateForge records real user journeys from the legacy PHP application (responses, database changes, and outbound messages). A path invented in a workshop is not a recorded journey.

During parity, the same journeys are replayed against PHP and the generated Java 21 / Spring Boot application in a deterministic sandbox.

## The three parity numbers

Each published SUCCEEDED wave reports three percentages. A wave only closes when **all three are 100** and write-effect differences are **0**:

| Measure | Meaning |
| --- | --- |
| Fixture | Share of compared fixtures whose HTTP responses matched |
| De-duplicated | Share of distinct journeys after de-duplication |
| Route-weighted | Match rate weighted by route coverage of the capture |

Unscored fixtures (shown as coverage gaps on the proof page) are left out of the match. Where the cause is recorded, they are legacy PHP 500 responses from the PHP application — not target Java regressions.

## Write-effect gate

Parity also compares database mutations and outbound API payloads. **Write-effect differences must be 0** before a wave is marked SUCCEEDED.

## Auth / CSRF and quality

Published waves ran auth and CSRF sweeps. Gate quality on the published close: **0 critical**, **0 HIGH** findings.

## Application waves vs Q07

| Suite | What it proves |
| --- | --- |
| WA Blast Pro waves 1–2 | Plain PHP multi-tenant SaaS migration on recorded journeys |
| InvoicePlane waves 1–2 | CodeIgniter 3.4 public OSS benchmark on recorded journeys |
| Q07 CI3 conformance | Java adapter behaves like CodeIgniter 3 APIs (83 fixtures) |

Q07 is **not** one of the four application migration waves. Do not add its 83 fixtures into the 858 journey total.

## Sanitization

This repository publishes **scorecards only**. It does not redistribute:

- application source (except pointing at public InvoicePlane upstream)
- captures, HAR files, or fixture bodies
- internal run IDs, LLM spend, or local paths

## Honest middle (InvoicePlane wave 2)

A finished 100/100/100 figure alone does not show effort. On InvoicePlane wave 2 (49 units, 1,667 lines of PHP across six CRUD modules), the first full three-way comparison after the generated application would start matched **82%** of distinct journeys. Hand fixes reached **100%** at **9.7** fixes per 1,000 lines of PHP — mostly adapter-layer fixes that benefit the next CodeIgniter application. That story is also on the proof page.

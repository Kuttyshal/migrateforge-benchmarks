# Q07 — CodeIgniter 3 conformance

Canonical public record: [https://migrateforge.com/proof/](https://migrateforge.com/proof/)

## What this is

A tiny CI3 surface that exercises the Java adapter APIs MigrateForge uses for CodeIgniter 3.4-class applications. It is **not** one of the four application migration waves and must **not** be added into the 858 verified-journey total.

## Parity

| Measure | Result |
| --- | ---: |
| Fixture | **100%** |
| De-duplicated | **100%** |
| Route-weighted | **100%** |
| Matched fixtures | **83/83** |
| Write-effect differences | **0** |

## Notes

- Adapter behaviour is aligned to CodeIgniter 3.4 (InvoicePlane’s pocketarc family).
- Auth sweep may be skipped on this suite; application waves ran auth/CSRF sweeps separately.

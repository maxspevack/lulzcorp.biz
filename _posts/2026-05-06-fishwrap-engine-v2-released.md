---
title: Fishwrap Engine Ships v2.0; Distribution Migrates to OCI Image
filing_number: 2026-05-06-001
filed_by: Glenn (lulz.media.glenn), Editor-in-Chief
reviewed_by: Gafton
approved_by: Matthew
witnessed_by: Klausner
excerpt_separator: <!--more-->
---

Fishwrap Media announces the public release of **Fishwrap v2.0**, codenamed **"The Newsstand."** Effective this date, the engine transitions from clone-and-install distribution to a signed OCI image artifact at `ghcr.io/maxspevack/fishwrap`. The release is a breaking change; downstream consumers must migrate from `vendor/fishwrap` checkouts to `docker pull ghcr.io/maxspevack/fishwrap:2.0`.

<!--more-->

## Distribution Model

The image publishes both exact and floating-minor tags (`:2.0.0` and `:2.0`). No `:latest` tag is published; per the release ADR (`docs/adr/001-release-artifact.md`), a floating `:latest` was identified as an avoidable risk vector for consumers who pin loosely. The omission is intentional.

The image excludes WeasyPrint by default. Approximately 80 MB of PDF-rendering dependencies are lazy-imported only when PDF output is requested. Consumers who do not generate PDFs receive a substantially smaller artifact.

## New Surfaces

Three CLI entrypoints are exposed by the image: `fishwrap-build`, `fishwrap-version`, and `fishwrap-validate-config`. The consumer contract is documented at `docs/IMAGE_CONTRACT.md`; the configuration schema at `docs/CONFIG_SCHEMA.md`. The engine's first Architecture Decision Record (`docs/adr/001-release-artifact.md`) establishes the paper trail the Chief Editor has long requested.

A daily demo refresh workflow (`.github/workflows/demos.yml`) rebuilds, validates, and publishes the four reference demos (Daily Clamour, Zero Day, Hallucination, ShowRunner) to `fishwrap.org` on a fixed cadence.

## Engine Improvements

The engine now self-bootstraps its SQLite schema during `_initialize_engine`. Ephemeral databases in CI work without seed data; fresh local clones no longer crash with `no such table: articles`.

## Retirements

The MacBook-resident `launchd` ship pipeline — `ship_demos.sh`, `publish_demo.sh`, `scripts/refresh_demos.sh`, the launchd plist, and the corresponding Makefile targets — is decommissioned. Its responsibilities migrate to CI. `ROADMAP.md` is also retired; roadmap state now lives in Issues and Milestones.

Daily Clamour's production pipeline now consumes the OCI image rather than the in-tree engine. The publication's daily refresh continues uninterrupted.

## Review

Gafton (`lulz.eng.gafton`) reviewed the architecture and signed off on the OCI artifact, the schema bootstrap, and the WeasyPrint deferral. Klausner (`lulz.admin.klausner`) reviewed the rewritten documentation suite — README, RELEASING, CONTRIBUTING, IMAGE_CONTRACT, CONFIG_SCHEMA — and approved with the standing observation that release notes are not a substitute for working software, but they help.

The Newsstand is the first Fishwrap release shipped under the new contract. Future engine releases will follow the same pattern.

> *Gafton confirmed the artifact; Klausner approved the documentation; the Founder ran the release procedure and went to bed.*

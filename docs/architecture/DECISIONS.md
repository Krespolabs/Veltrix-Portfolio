# Architecture Decision Records

This file records material technical and product decisions. Add new decisions rather than silently rewriting the history.

## ADR-001: GitHub is the source of truth
- **Status:** Accepted
- **Date:** 2026-10-30
- **Context:** The portfolio must present work across several repositories without creating conflicting records.
- **Decision:** GitHub remains canonical for source code, documentation, issues, pull requests, and release history. The portfolio repository stores curated public-facing metadata and editorial content.
- **Consequences:** Website content may summarize linked repositories, but must not replace their authoritative documentation. Synchronization must respect visibility and approval rules.

## ADR-002: Next.js and TypeScript are the planned web stack
- **Status:** Accepted for implementation planning
- **Date:** 2026-10-30
- **Context:** The portfolio needs a maintainable, performant application with strong content and routing support.
- **Decision:** Use Next.js App Router and TypeScript, with Tailwind CSS for styling.
- **Consequences:** Confirm current stable versions and project conventions when scaffolding. This decision does not imply the application already exists.

## ADR-003: Evidence-led project status
- **Status:** Accepted
- **Date:** 2026-10-30
- **Context:** Portfolio credibility depends on distinguishing working software from plans and prototypes.
- **Decision:** Every project uses an explicit lifecycle status and supporting evidence. Do not label a project Live without a verified public deployment.
- **Consequences:** Project pages must include limitations and last-verified information where practical.

## ADR-004: Public-first, privacy-safe publication
- **Status:** Accepted
- **Date:** 2026-10-30
- **Context:** The GitHub account contains both public and private work.
- **Decision:** Only explicitly approved public information may be published. Private repository data is excluded by default.
- **Consequences:** Any future connector or API integration must enforce an allowlist and avoid private data exposure.

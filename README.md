# Agent Skills

A collection of agent skills that extend capabilities across planning, development, and tooling.

## Planning & Design

These skills help you think through problems before writing code.

- **to-prd** — Turn the current conversation context into a PRD and submit it as a GitHub issue. No interview — just synthesizes what you've already discussed.

- **to-issues** — Break any plan, spec, or PRD into independently-grabbable GitHub issues using tracer-bullet vertical slices. Presents a proposed breakdown and iterates with you before creating issues.

- **grill-me** — Get relentlessly interviewed about a plan or design until every branch of the decision tree is resolved. Asks one question at a time and explores the codebase when it can answer for itself.

- **design-an-interface** — Generate multiple radically different interface designs for a module using parallel sub-agents. Based on "Design It Twice" from _A Philosophy of Software Design_.

- **request-refactor-plan** — Create a detailed refactor plan with tiny commits via user interview, then file it as a GitHub issue with a full decision document and testing decisions.

- **domain-model** — Stress-test a plan against the existing domain model. Challenges terminology, sharpens fuzzy language, updates `CONTEXT.md` and ADRs inline as decisions crystallize.

## Development

These skills help you write, refactor, and fix code.

- **tdd** — Test-driven development with a red-green-refactor loop. Builds features or fixes bugs one vertical slice at a time. Enforces behavior-focused tests through public interfaces only.

- **triage-issue** — Investigate a bug by exploring the codebase, identify the root cause, and file a GitHub issue with a TDD-based fix plan. Mostly hands-off — minimal questions to the user.

- **improve-codebase-architecture** — Find deepening opportunities in a codebase, informed by the domain language in `CONTEXT.md` and the decisions in `docs/adr/`. Surfaces shallow modules and proposes refactors that improve testability and AI-navigability.

- **migrate-to-shoehorn** — Migrate test files from `as` type assertions to `@total-typescript/shoehorn`. Replaces `as Type` with `fromPartial()` and `as unknown as Type` with `fromAny()`.

- **scaffold-exercises** — Create exercise directory structures with sections, problems, solutions, and explainers that pass linting.

## Issue Tracking & QA

- **github-triage** — Triage GitHub issues through a label-based state machine (`needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`). Supports overview, per-issue deep-dive, and quick state overrides.

- **qa** — Interactive QA session where you describe bugs conversationally and the agent files properly structured GitHub issues. Explores the codebase in the background to pick up domain language.

## Tooling & Setup

- **setup-pre-commit** — Set up Husky pre-commit hooks with lint-staged, Prettier, type checking, and tests.

- **git-guardrails** — Set up Claude Code hooks to block dangerous git commands (`git push`, `git reset --hard`, `git clean`, `git branch -D`, etc.) before they execute. Configurable at project or global scope.

## Writing & Knowledge

- **write-a-skill** — Create new skills with proper structure, progressive disclosure, and bundled resources.

- **edit-article** — Edit and improve articles by restructuring sections, improving clarity, and tightening prose.

- **ubiquitous-language** — Extract a DDD-style ubiquitous language glossary from the current conversation. Flags ambiguities, proposes canonical terms, and saves to `UBIQUITOUS_LANGUAGE.md`.

- **obsidian-vault** — Search, create, and manage notes in an Obsidian vault with wikilinks and index notes.

- **domain-model** — _(Also listed under Planning & Design)_ — grills against the existing glossary and keeps `CONTEXT.md` up-to-date.

## Utilities

- **caveman** — Ultra-compressed communication mode. Cuts token usage ~75% by dropping filler, articles, and pleasantries while keeping full technical accuracy. Stays active until explicitly turned off.

- **zoom-out** — Tell the agent to go up a layer of abstraction and give a map of all relevant modules and callers. Use when unfamiliar with a section of code or need to see how it fits into the bigger picture.

- **truth** — Unfiltered, direct feedback without ego protection. No hedging, no sandwich feedback. Active for the entire conversation once invoked.

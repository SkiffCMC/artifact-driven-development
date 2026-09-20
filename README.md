# Artifact-Driven Development (ADD)

**Artifact-Driven Development (ADD)** is a meta-architecture that maps a strict 7-layer **Artifact Layers (AL)** model onto an AI-driven software engineering workflow. ADD solves the "context collapse" (hallucination) problem in LLM-generated code by enforcing strict top-down encapsulation of artifacts across engineering strata (AL7 → AL1).

In the ADD paradigm, source code (AL2) ceases to be the Source of Truth and becomes a transient compilation artifact. The human engineer assumes the role of a **Meta-Orchestrator**, focusing entirely on designing architectural blueprints (AL4 Specs) and strict, deterministic Black-box contracts (AL5 Loot Filters). If the artifact stack resolves cleanly, the feature is ready.

---

## Framework: 7-Layer Artifact Layers (AL)

All development in this project flows strictly top-down (AL7 → AL1). Skipping layers is strictly prohibited.

* **AL 7 (Intent):** Abstract stakeholder or user business intent. (Format: Unstructured text, support tickets).
* **AL 6 (Requirements):** Formalized User Stories, Acceptance Criteria (AC), and Ubiquitous Language. (Format: Markdown).
* **AL 5 (Contracts):** Zero-trust boundaries. Strict interfaces, Zod schemas, E2E/Playwright tests, data-qa dictionaries, OpenAPI. (Format: TypeScript / JSON).
* **AL 4 (Design):** Architectural blueprints, pattern selection, database schemas (Drizzle/Objection), and Temporal worker pipelines (SpecDD). (Format: Markdown Spec).
* **AL 3 (Context):** Context routing. Highly specific prompts aggregating upper-level artifacts for code-generation agents. (Format: Text).
* **AL 2 (Implementation):** Source code, database migrations, and unit tests translated via TDD. (Format: TS, SQL).
* **AL 1 (Runtime):** Physical execution environment. V8 Engine, PostgreSQL, Compilers.

---

## License Notice

*The ADD methodology text, documentation, and architecture diagrams are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code snippets, configuration templates, and `.cursorrules` are licensed under the MIT License.*

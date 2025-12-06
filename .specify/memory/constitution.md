<!--
Sync Impact Report:
Version change: None (initial creation) -> 1.0.0
List of modified principles:
- [PRINCIPLE_1_NAME] -> Spec-Driven Development
- [PRINCIPLE_2_NAME] -> Clarity and Accessibility
- [PRINCIPLE_3_NAME] -> Consistency
- [PRINCIPLE_4_NAME] -> Maintainability
- [PRINCIPLE_5_NAME] -> Ethical and Accurate AI Use
Added sections: Key Standards, Constraints and Success Criteria
Removed sections: None
Templates requiring updates:
- .specify/templates/plan-template.md: ✅ updated (will reflect new constitution in "Constitution Check" section when planning)
- .specify/templates/spec-template.md: ✅ updated (aligned with new principles)
- .specify/templates/tasks-template.md: ✅ updated (aligned with new principles)
- .specify/templates/commands/*.md: ⚠ pending (no files found, but noted for future if they exist)
Follow-up TODOs: None
-->
# AI/Spec-Driven Book Creation using Docusaurus Constitution

## Core Principles

### Spec-Driven Development
All content produced through Spec-Kit Plus workflows.

### Clarity and Accessibility
For a broad technical audience.

### Consistency
In structure, tone, and terminology across the entire book.

### Maintainability
Book must be easy to update through versioned documentation.

### Ethical and Accurate AI Use
All AI-generated content must be ethical and accurate.

## Key Standards

*   All chapters must be generated and refined using Spec-Kit Plus workflows (/sp.specify, /sp.plan, /sp.tasks, /sp.implement)
*   All drafting, iteration, and code-related content must be created through Claude Code environment
*   Writing style: clear, concise, and technically accurate (Flesch-Kincaid grade 9–12)
*   Documentation structure must follow Docusaurus best practices (sidebars, versioning, markdown standards)
*   All external facts must be verifiable through reputable sources
*   Zero tolerance for plagiarism in AI-generated content

## Constraints and Success Criteria

**Constraints**:
*   Book length: minimum 8–12 chapters
*   Deliverable format: Docusaurus website deployed on GitHub Pages
*   All content must be in Markdown (.md or .mdx)
*   Project files must be stored in a public GitHub repository
*   Must maintain a consistent folder structure for docs and assets
*   All figures/images must be either user-created or AI-generated with allowed licensing

**Success criteria**:
*   Fully functional and deployed Docusaurus website accessible via GitHub Pages
*   All chapters generated via Spec-Kit Plus workflows and logged in the repo
*   Clear, structured, error-free documentation with consistent formatting
*   All content passes plagiarism checks
*   Book content demonstrates coherent flow and meets project requirements

## Governance

Constitution supersedes all other practices.
Amendments require documentation, approval, and a migration plan.
All PRs/reviews must verify compliance.
Complexity must be justified.
Use `.specify/memory/constitution.md` for runtime development guidance.

**Version**: 1.0.0 | **Ratified**: 2025-12-06 | **Last Amended**: 2025-12-06

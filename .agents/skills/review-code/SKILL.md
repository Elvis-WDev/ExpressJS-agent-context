---
name: review-code
description: Use when reviewing changes for bugs, security risks, architecture drift, missing tests, and documentation gaps.
---

# Review Code

## Context To Load

Read:

- `AGENTS.md`
- `docs/quality/code-review.md`
- Relevant architecture docs.
- Relevant feature specification and acceptance criteria.

## Review Stance

Lead with findings. Prioritize:

1. Bugs and data loss.
2. Security and auth issues.
3. Behavioral regressions.
4. Missing tests or verification.
5. Architecture drift.

## Output Format

- Findings first, ordered by severity.
- Include file and line references.
- Add open questions after findings.
- Keep summaries secondary.

If no issues are found, say so clearly and mention residual risk.


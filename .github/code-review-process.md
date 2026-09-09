# Collaborative Code Review Process

Use this process to coordinate review across technical teammates, less technical teammates, and Copilot.

## Goals

1. Good coverage for changed behavior
2. High code quality and maintainability
3. Security-focused review on every change
4. Low review and iteration cost

## Roles

- **Author**: implements the change, prepares context, requests review.
- **Copilot reviewer**: catches code-level issues quickly and consistently.
- **Technical reviewer**: validates architecture, edge cases, and correctness.
- **Less technical reviewer**: validates business intent, wording, UX, and clarity.

## Standard review flow

1. **Author self-check**
   - Run or update relevant tests for changed behavior.
   - Manually verify changed user flows.
   - Confirm no secrets are introduced.
2. **Copilot review**
   - Request local review in VS Code and/or PR review in GitHub.
   - Address actionable comments and re-request review after substantial updates.
3. **Human review**
   - Request at least one technical reviewer.
   - Request at least one less technical reviewer for user-facing changes.
4. **Merge readiness**
   - Resolve review conversations.
   - Confirm PR template checklist is complete.

## Review focus areas

### Coverage

- New or changed behavior has tests when practical.
- Edge cases are validated (through tests or clear manual verification notes).

### Quality

- Code is readable and maintainable.
- Duplication is minimized.
- Errors are handled explicitly.

### Security

- Inputs are validated and sanitized.
- Auth and permission boundaries are respected.
- Secrets are not hardcoded or committed.

### Cost minimization

- Keep PRs small and focused.
- Use branch/ruleset automation to reduce manual coordination.
- Re-request Copilot review only after meaningful code changes.


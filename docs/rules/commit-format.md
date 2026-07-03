# Commit Format

## Pattern

```text
<type>[optional scope]: [LINEAR-ISSUE] <description>
```

- Linear issue extracted from the current branch name. If no match, default to `CDC-00`.
- Description: imperative mood, lowercase first word, no trailing period, under 100 characters.
- Always use git conventional commit format.
- No direct commits to `master` — always use a feature branch and PR.
- No `[skip ci]` in manual commits — reserved for automated changelog updates.
- When a breaking change happen, a `!` should be added according to the conventional commit format

## Examples

```text
fix(8.3): [CDC-123] Fix duplicate warnings when connection error
fix(core)!: [CDC-93] Fix duplicate message delivery
chore(8.1): [CDC-23] Bump `glob` to v10.3.12
feat(8.3): [CDC-124] Add a tag tree browse
```

## PR Titles

PR titles follow the same `<type>[optional scope]: [LINEAR-ISSUE] <description>` pattern as commit messages.

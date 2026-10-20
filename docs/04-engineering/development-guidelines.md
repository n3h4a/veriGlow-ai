# Development Guidelines

| | |
|---|---|
| **Status** | 🟡 Draft — workflow rules apply now; code rules finalised once the stack is chosen |
| **Phase** | 5 — MVP Development |

---

## 1. Branching

- `main` is always deployable and protected.
- Work happens on short-lived branches: `feat/`, `fix/`, `docs/`, `chore/`, `research/`.
- Merge via pull request only.

## 2. Commits

[Conventional Commits](https://www.conventionalcommits.org/):

```text
<type>(<scope>): <summary>
```

| Type | Use for |
|---|---|
| `feat` | New functionality |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `test` | Adding or fixing tests |
| `refactor` | Code change with no behaviour change |
| `chore` | Tooling, config, dependencies |

## 3. Pull Requests

- One logical change per PR.
- Use the [PR template](../../.github/pull_request_template.md).
- Link the related issue.
- Self-review before requesting review.

## 4. Definition of Done

A change is done when:

- [ ] It meets the acceptance criteria of its issue.
- [ ] Tests are written and passing.
- [ ] Documentation is updated.
- [ ] It has been reviewed and merged.
- [ ] `CHANGELOG.md` is updated for user-visible changes.

## 5. Code Standards (to be completed after stack ADRs)

- Language style guides and formatters
- Linting rules
- Project layout conventions
- Error handling and logging conventions

## 6. Secrets

- Never commit secrets. Use environment variables.
- Document required variables in a `.env.example` file once the backend exists.

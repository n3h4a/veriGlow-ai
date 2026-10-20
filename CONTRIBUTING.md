# Contributing to VeriGlow-ai

Thanks for your interest in VeriGlow-ai. The project is currently in its **research phase**, so the most valuable contributions right now are evidence, feedback on documents, and well-reasoned challenges to assumptions.

## Ways to Contribute

| Contribution | How |
|---|---|
| Report a problem in a document or (later) the code | Open a **Bug report** issue |
| Suggest a feature or research direction | Open a **Feature request** issue |
| Share evidence (articles, studies, data) | Open an issue and link the source |
| Improve documentation | Open a pull request |

## Workflow

1. **Open an issue first** for anything beyond a typo, so the approach can be agreed before work starts.
2. **Create a branch** from `main`:

   | Prefix | Use for |
   |---|---|
   | `feat/` | New functionality |
   | `fix/` | Bug fixes |
   | `docs/` | Documentation |
   | `chore/` | Tooling, config, housekeeping |
   | `research/` | Research documents |

   Example: `docs/competitor-analysis`

3. **Commit using [Conventional Commits](https://www.conventionalcommits.org/):**

   ```text
   <type>(<optional scope>): <short summary in imperative mood>
   ```

   Examples:

   ```text
   docs(research): add competitor feature comparison table
   feat(verification): add batch code parser
   fix(api): return 404 for unknown product id
   ```

4. **Open a pull request** using the PR template. Keep PRs small and focused on one change.

## Documentation Standards

- GitHub-flavoured Markdown.
- Every claim backed by a source should link to it.
- Mark assumptions explicitly as assumptions.
- Use tables for comparisons and Mermaid for diagrams.

## Decision Records

Significant technical or product decisions are recorded as ADRs in [`docs/07-decisions/`](docs/07-decisions/). Copy [`ADR-template.md`](docs/07-decisions/ADR-template.md), number it sequentially, and include it in your PR.

## Code of Conduct

Be respectful, assume good intent, and critique ideas rather than people.

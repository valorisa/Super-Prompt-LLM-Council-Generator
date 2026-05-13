# Contributing to Super-Prompt-LLM-Council-Generator

Thank you for your interest in contributing! Here are the guidelines.

## Branching Strategy

```text
main   ← Production branch (stable, tagged)
  │
  └── dev  ← Integration branch (next version)
        │
        ├── feat/your-feature    ← New feature
        ├── fix/bug-name         ← Bug fix
        └── docs/update-docs     ← Documentation update
```

## Contribution Workflow

1. **Fork** the repository
2. **Clone** your fork:

   ```bash
   git clone https://github.com/YOUR_USERNAME/Super-Prompt-LLM-Council-Generator.git
   cd Super-Prompt-LLM-Council-Generator
   ```

3. **Create a branch** from `dev`:

   ```bash
   git checkout dev
   git checkout -b feat/your-feature-name
   ```

4. **Make your changes** and test them
5. **Commit** with conventional commit messages:

   ```bash
   git commit -m "feat: add new example for data science use case"
   ```

6. **Push** to your fork:

   ```bash
   git push origin feat/your-feature-name
   ```

7. **Open a Pull Request** to the `dev` branch

## Commit Message Conventions

| Prefix | Usage | Example |
| --- | --- | --- |
| `feat:` | New feature | `feat: add cybersecurity analyst example` |
| `fix:` | Bug fix | `fix: correct markdown syntax in README` |
| `docs:` | Documentation | `docs: update installation instructions` |
| `refactor:` | Code refactoring | `refactor: simplify circle validation logic` |
| `test:` | Tests | `test: add validation for proxy variables` |
| `chore:` | Maintenance | `chore: update dependencies` |

## Code Quality

- All Markdown files must pass `markdownlint` checks
- Follow the existing style and structure
- Test your examples before submitting
- Update documentation if needed

## Questions?

Open an issue or start a discussion. We're here to help!

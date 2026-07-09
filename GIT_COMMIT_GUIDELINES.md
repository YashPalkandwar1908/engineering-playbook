# Git Commit Guidelines

## Commit Message Format

Follow the Conventional Commits specification with a concise summary and a descriptive body.

```text
<type>: <short summary>

- Bullet 1
- Bullet 2
- Bullet 3
...
```

### Guidelines

* Keep the first line short (ideally under 72 characters).
* Use the imperative mood (e.g., "add", "implement", "fix", "update").
* Explain **what** changed in the body.
* Each bullet should describe one logical change.
* Group related changes into a single commit.

---

# Commit Types

| Type        | Use For                                               |
| ----------- | ----------------------------------------------------- |
| `feat:`     | New functionality or features                         |
| `fix:`      | Bug fixes                                             |
| `refactor:` | Internal code restructuring without changing behavior |
| `docs:`     | Documentation changes only                            |
| `test:`     | Adding or updating tests                              |
| `chore:`    | Tooling, configuration, dependencies, maintenance     |
| `perf:`     | Performance improvements                              |
| `build:`    | Build system or dependency changes                    |
| `ci:`       | CI/CD or workflow changes                             |
| `style:`    | Formatting or style changes with no logic changes     |
| `revert:`   | Reverting a previous commit                           |

---

# Commit Examples

## Project Initialization

```text
chore: initialize development environment

- Set up project structure
- Configure dependency management
- Configure code formatting and linting
- Configure testing framework
- Add CI workflow
```

---

## New Feature

```text
feat: implement authentication service

- Add authentication module
- Implement login workflow
- Add token validation
- Add unit tests
```

---

## Bug Fix

```text
fix: handle invalid configuration values

- Validate configuration before loading
- Improve error messages
- Add regression tests
```

---

## Refactoring

```text
refactor: simplify configuration loading

- Remove duplicate logic
- Extract helper functions
- Improve module organization
```

---

## Documentation

```text
docs: add architecture overview

- Document system architecture
- Add component diagram
- Describe project structure
```

---

## Testing

```text
test: add unit tests for configuration

- Add configuration loading tests
- Add validation tests
- Improve test coverage
```

---

## CI/CD

```text
ci: add continuous integration workflow

- Run formatter checks
- Run linter
- Run type checking
- Execute test suite
```

---

## Performance

```text
perf: optimize cache lookups

- Reduce redundant computations
- Improve cache hit rate
- Update benchmarks
```

---

# Best Practices

* One logical change per commit.
* Commit frequently with meaningful messages.
* Keep commits focused and easy to review.
* Ensure the project builds and tests pass before committing.
* Avoid mixing unrelated changes in a single commit.
* Use the commit body to provide context when necessary.

---

# Version Tags

Create version tags at significant milestones or releases.

```bash
git tag v0.1.0
git push origin v0.1.0
```

Examples:

```text
v0.1.0
v0.2.0
v0.3.0
v1.0.0
```

For milestone-based development, use pre-release tags when appropriate:

```text
v0.1.0-m1
v0.1.0-m2
v0.1.0-m3
```

Push a new tag with:

```bash
git push origin <tag-name>
```

---

# Commit Checklist

Before every commit:

* Code compiles successfully.
* Tests pass.
* Formatting has been applied.
* Linting passes.
* Type checking passes (if applicable).
* Documentation is updated when needed.
* Commit message follows the project standard.

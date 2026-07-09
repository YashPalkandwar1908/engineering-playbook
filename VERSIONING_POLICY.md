# Versioning Policy

## 1. Overview

This project follows **Semantic Versioning (SemVer)**.

Version format:

```
MAJOR.MINOR.PATCH
```

Examples:

```
0.1.0
0.2.0
0.3.0
1.0.0
1.2.3
2.0.0
```

---

# 2. Semantic Versioning

## MAJOR

Increment when introducing incompatible or breaking changes.

Examples:

```
1.0.0 → 2.0.0
```

Example scenarios

- API redesign
- Breaking database schema
- Removing public interfaces
- Renaming configuration formats

---

## MINOR

Increment when adding backward-compatible functionality.

Examples

```
0.2.0 → 0.3.0

1.4.0 → 1.5.0
```

Example scenarios

- New feature
- New module
- New REST endpoint
- New plugin
- New AI capability

---

## PATCH

Increment when fixing bugs without adding new functionality.

Examples

```
0.3.1 → 0.3.2

1.5.2 → 1.5.3
```

Example scenarios

- Bug fixes
- Documentation fixes
- Small optimizations
- Performance improvements

---

# 3. Development Milestones

During development, milestone tags mark internal checkpoints.

Format

```
v<major>.<minor>.<patch>-m<milestone>
```

Examples

```
v0.1.0-m1
v0.1.0-m2
v0.1.0-m3
v0.2.0-m1
```

Example

```
v0.1.0-m1

• Repository created
• Project structure
• CI pipeline
• Development tooling
```

---

```
v0.1.0-m2

• Configuration system
• Logging
• Error handling
• Unit testing
```

---

```
v0.1.0-m3

• Event Bus
• Result Objects
• Service Registry
```

---

# 4. Stable Releases

After completing several milestones, publish a stable release.

Example

```
v0.1.0
```

Release Title

```
ProjectName v0.1.0 – Platform Foundation
```

Release Includes

```
• Configuration System
• Logging
• Error Handling
• Event Bus
• Unit Tests
```

---

Another example

```
v0.2.0
```

Release Includes

```
• Plugin System
• Scheduler
• Workflow Engine
```

---

# 5. Git Tags

Create an annotated tag.

```
git tag -a v0.1.0-m2 -m "Milestone 2 completed"
```

Push a single tag.

```
git push origin v0.1.0-m2
```

Push all tags.

```
git push --tags
```

Verify tags.

```
git tag
```

Example output

```
v0.1.0-m1
v0.1.0-m2
v0.1.0
```

---

# 6. GitHub Releases

Every stable version should have a GitHub Release.

Release Structure

```
Title

Summary

Highlights

Added

Changed

Fixed

Removed

Breaking Changes

Migration Guide

Known Issues

Contributors
```

Example

```
Title

ResearchOS v0.1.0 – Platform Foundation
```

---

# 7. CHANGELOG

Every stable release updates CHANGELOG.md.

Example

```
# Changelog

## v0.2.0

### Added

- Plugin Manager
- Workflow Engine

### Changed

- Improved scheduler

### Fixed

- Event dispatch bug
```

---

# 8. Recommended Workflow

Example

```
Complete Feature
        │
        ▼
Run Tests
        │
        ▼
Commit Changes
        │
        ▼
Create Milestone Tag
        │
        ▼
Continue Development
        │
        ▼
Complete Multiple Milestones
        │
        ▼
Update CHANGELOG.md
        │
        ▼
Create GitHub Release
        │
        ▼
Start Next Version
```

---

# 9. Example Project Timeline

```
v0.1.0-m1
│
├── Project setup
├── Repository
└── CI

↓

v0.1.0-m2
│
├── Configuration
├── Logging
└── Error Handling

↓

v0.1.0-m3
│
├── Event Bus
├── Service Registry
└── Tests

↓

v0.1.0
│
Stable Release

↓

v0.2.0-m1
│
├── Plugin System

↓

v0.2.0
│
Stable Release

↓

v1.0.0
│
Production Ready
```

---

# 10. Best Practices

- Follow Semantic Versioning.
- Use annotated Git tags.
- Publish GitHub Releases only for stable versions.
- Maintain CHANGELOG.md.
- Write clear release notes.
- Ensure tests pass before tagging.
- Never modify published tags.
- Keep release history traceable.

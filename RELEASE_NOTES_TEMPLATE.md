# Release Notes Template

Every public release should include release notes following this structure.

---

# Release Title

```text
<Project Name> v<Version> – <Release Name>
```

Example:

```text
ResearchOS v0.1.0 – Platform Foundation
```

---

# Summary

Provide a brief overview of what this release delivers.

**Example**

```text
This release establishes the platform foundation for ResearchOS. It introduces the core project infrastructure, development tooling, continuous integration, and essential platform services required for future development.
```

---

# Highlights

Summarize the most important additions.

**Example**

```text
• Platform foundation completed
• Development environment established
• Continuous Integration configured
• Project architecture finalized
```

---

# Added

List all new functionality introduced in this release.

**Example**

```text
- Configuration management
- Structured logging
- Error hierarchy
- Event bus
- Result objects
- Project templates
```

---

# Changed

Describe improvements or modifications to existing functionality.

**Example**

```text
- Consolidated tool configuration into pyproject.toml
- Simplified project package layout
- Renamed core package to kernel
```

---

# Fixed

Document resolved bugs.

**Example**

```text
- Fixed CI dependency installation
- Fixed formatting inconsistencies
- Corrected project configuration
```

---

# Removed

Document removed or deprecated functionality.

**Example**

```text
- Removed legacy configuration files
- Removed duplicate tool configuration
```

If nothing was removed, simply write:

```text
None
```

---

# Breaking Changes

Describe any incompatible changes.

**Example**

```text
- Renamed API endpoints
- Updated configuration format
- Package imports changed
```

If there are no breaking changes:

```text
None
```

---

# Migration Guide

If users need to perform any steps before upgrading, explain them here.

**Example**

```text
1. Update project dependencies.
2. Rename configuration files.
3. Run database migrations.
```

If no migration is required:

```text
No migration required.
```

---

# Testing

Summarize how the release was validated.

**Example**

```text
- Unit tests passed
- Integration tests passed
- Static type checking passed
- Linting passed
- Formatting verified
```

---

# Documentation

Mention documentation updates.

**Example**

```text
- Updated README
- Added architecture documentation
- Updated API reference
```

---

# Known Issues

List any known limitations.

**Example**

```text
- Plugin API is experimental.
- Windows support is partially tested.
```

If there are no known issues:

```text
None
```

---

# Contributors

Recognize contributors.

**Example**

```text
- John Doe
- Jane Smith
```

For a solo project:

```text
- Yash Palkandwar
```

---

# Full Changelog

Provide a link to the project's changelog.

**Example**

```text
See CHANGELOG.md for the complete list of changes.
```

---

# Example Release

```text
ResearchOS v0.1.0 – Platform Foundation

Summary

This release establishes the initial platform foundation for ResearchOS. It introduces the core project structure, development tooling, and quality assurance pipeline.

Highlights

• Project architecture completed
• CI pipeline established
• Development tooling configured
• Initial platform package created

Added

- Project directory structure
- pyproject.toml
- Pre-commit hooks
- Ruff
- Black
- MyPy
- Pytest
- GitHub Actions

Changed

- Consolidated all tool configuration into pyproject.toml

Fixed

- CI dependency installation

Removed

- Standalone Ruff configuration
- Standalone MyPy configuration
- Standalone Pytest configuration

Breaking Changes

None

Migration Guide

No migration required.

Testing

- Ruff passed
- Black passed
- MyPy passed
- Pytest passed

Documentation

- Added Git commit guidelines
- Added versioning policy
- Updated README

Known Issues

None

Contributors

- Yash Palkandwar

Full Changelog

See CHANGELOG.md
```

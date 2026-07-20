# Milestone-Based Code Delivery

## Objective

Optimize for **milestone completion** instead of incremental file delivery.

A **milestone** is a complete, testable unit of functionality that can be copied, pasted, and run with minimal developer effort.

Examples:

* PDF to JPG Converter
* Images to PDF Converter
* PDF Merger
* Authentication Module
* REST API
* Dashboard UI

The goal is to minimize:

* AI responses
* Copy-paste operations
* Manual editing
* Context switching

---

# Delivery Strategy

## Preferred

Return **every file required for the milestone** in **one PowerShell code block**.

Example milestone:

```
PDF Merger

Files
├── run.py
├── src/gui/main_window.py
├── src/core/merge_pdf.py
├── requirements.txt
└── README.md
```

Return:

```powershell
@'
...
'@ | Set-Content ...

@'
...
'@ | Set-Content ...

python run.py
```

The developer should be able to:

1. Copy once.
2. Paste once.
3. Run once.
4. Test immediately.

---

## If the Milestone Is Too Large

If the complete milestone cannot fit into one response:

* Split it into **at most two PowerShell code blocks**.
* Organize the files logically.

Example:

### Block 1

* Core
* UI
* Configuration

### Block 2

* Remaining files
* Tests
* Documentation

Avoid any additional blocks unless explicitly requested.

---

# Complete Files Only

Always return **complete file contents**.

Do **not** return:

* Partial snippets
* Patch-style edits
* "Replace this function"
* "Insert below line 42"
* Diffs

Preferred format:

```powershell
@'
Complete file contents
'@ | Set-Content -Encoding utf8 src\example.py

code -r src\example.py
```

Every file should be immediately usable without manual editing.

---

# Finish the Entire Milestone

Do not stop halfway through a feature.

If the milestone includes:

* UI
* Backend
* Utilities
* Configuration
* Documentation
* Startup scripts

Return everything required for the milestone to run successfully.

---

# Developer Productivity Principles

Optimize every response to reduce developer effort.

Minimize:

* AI responses
* Copy-paste operations
* Manual edits
* Context switching

The ideal workflow is:

1. Copy one PowerShell block.
2. Paste it into the terminal.
3. Run the project.
4. Verify the milestone.

No additional editing should be required.

---

# Response Rules

* Deliver by **milestone**, not by individual file.
* Prefer **one PowerShell code block**.
* If necessary, use **no more than two PowerShell code blocks**.
* Always include **complete file contents**.
* Never return patches or partial snippets unless explicitly requested.
* Ensure the milestone is immediately testable.

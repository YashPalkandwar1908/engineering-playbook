# PowerShell File Operations

Reusable PowerShell commands for creating, updating, deleting, and managing project files.

---

# Create or Replace a File

Creates a new file or completely replaces an existing one.

```powershell
@'
File contents
'@ | Set-Content "path/to/file.py" -Encoding utf8

code -r "path/to/file.py"
```

---

# Append to a File

Adds new content to the end of an existing file.

```powershell
@'

Additional content
'@ | Add-Content "path/to/file.py" -Encoding utf8

code -r "path/to/file.py"
```

---

# Create an Empty File

```powershell
New-Item -ItemType File -Force "path/to/file.py"

code -r "path/to/file.py"
```

---

# Create Multiple Files

```powershell
New-Item -ItemType File -Force `
"path/file1.py", `
"path/file2.py", `
"path/file3.py"
```

---

# Create a Directory

```powershell
New-Item -ItemType Directory -Force "src/researchos/results"
```

---

# Create Multiple Directories

```powershell
New-Item -ItemType Directory -Force `
"docs/api", `
"docs/architecture", `
"docs/adr"
```

---

# Delete a File

```powershell
Remove-Item "path/to/file.py"
```

---

# Delete Multiple Files

```powershell
Remove-Item `
"path/file1.py", `
"path/file2.py"
```

---

# Delete a Directory

```powershell
Remove-Item "path/to/folder" -Recurse -Force
```

---

# Rename a File

```powershell
Rename-Item `
"old_name.py" `
"new_name.py"
```

---

# Move a File

```powershell
Move-Item `
"old/file.py" `
"new/file.py"
```

---

# Copy a File

```powershell
Copy-Item `
"source.py" `
"destination.py"
```

---

# Copy a Directory

```powershell
Copy-Item `
"src/researchos/results" `
"backup/results" `
-Recurse
```

---

# Open a File in VS Code

```powershell
code -r "path/to/file.py"
```

---

# Open Multiple Files

```powershell
code -r `
"src/file1.py" `
"tests/test_file1.py"
```

---

# Open the Current Project in VS Code

```powershell
code -r .
```

---

# Open Using the Default Windows Application

```powershell
ii "README.md"
```

`ii` is an alias for `Invoke-Item` and opens the file using its default Windows application.

---

# Display File Contents

```powershell
Get-Content "path/to/file.py"
```

---

# Check Whether a File Exists

```powershell
Test-Path "src/researchos/config/settings.py"
```

---

# List Files in a Directory

```powershell
Get-ChildItem "src/researchos"
```

---

# Create a File Only If It Doesn't Exist

```powershell
if (!(Test-Path "README.md")) {
    New-Item -ItemType File "README.md"
}
```

---

# Standard Workflow

For all project files (`.py`, `.md`, `.toml`, `.json`, `.yaml`, `.yml`, etc.), use the following pattern:

```powershell
@'
Complete file contents
'@ | Set-Content "path/to/file.ext" -Encoding utf8

code -r "path/to/file.ext"
```

Benefits:

* Creates the file if it doesn't exist.
* Replaces the file if it already exists.
* Saves using UTF-8 encoding.
* Opens the file immediately in the current VS Code window.

---

# Recommended Workflow

```
Create or Update File
        │
        ▼
Open in VS Code
        │
        ▼
Review Changes
        │
        ▼
Run Tests
        │
        ▼
Commit Changes
```

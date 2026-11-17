# Lab 5: Static Code Analysis — IT Helpdesk Ticket Allocator

**Name:** Aadya Arvind  
**SRN:** PES2UG24CS008  
**Section:** 5A CSE  
**Course:** Software Engineering

## Objective
Apply static code analysis tools to identify and fix code-quality issues, potential bugs, and security vulnerabilities in a Python IT Helpdesk Ticket Allocator.

## Problem Statement
IT Helpdesk Ticket Allocator — a Python program for creating, assigning, updating, prioritizing, and closing helpdesk tickets.

## Implementation
The program supports:
- Creating tickets with urgency levels from 1 to 5.
- Assigning tickets to technicians and adding notes.
- Identifying unassigned high-priority tickets.
- Closing tickets after admin password verification.
- Saving ticket information in JSON format.

The admin password is read from the `HELPDESK_ADMIN_PASSWORD` environment variable rather than being stored in the source code.

## Static Analysis Tools
- **Pylint:** Code quality and programming practices.
- **Bandit:** Potential security vulnerabilities.
- **Flake8:** Python style and formatting checks.

## Issues Addressed
- Replaced a mutable default argument with `None` and initialized the list within the function.
- Moved the admin password to an environment variable.
- Removed optional ping functionality that used `subprocess`.
- Added urgency validation (integer values from 1 to 5).
- Added checks for nonexistent ticket IDs.
- Used a context manager and UTF-8 encoding for file handling.
- Corrected formatting issues.

## Deliverables
- `helpdesk_system.py` — Updated IT helpdesk ticket allocator.
- `issues.md` — Identified issues and corresponding fixes.
- `reflection.md` — Responses to the lab reflection questions.
- `*_before.txt` and `*_after.txt` — Pylint, Bandit, and Flake8 analysis output files.
- `.gitignore` — Excludes the virtual environment and Python cache files.

## Report Notes
The final Pylint report records a score of **10.00/10**. The final Bandit report records **no issues identified**. The final Flake8 report file is empty. The original before-report files are retained unchanged.

## Setup and Execution
Create and activate a virtual environment, then install the analysis tools:

```bash
python -m venv venv
# Windows:
venv\\Scripts\\activate
# macOS/Linux:
source venv/bin/activate

python -m pip install pylint bandit flake8
```

Set the admin password for the current shell session:

```cmd
set HELPDESK_ADMIN_PASSWORD=your_password
```

Run the program:

```bash
python helpdesk_system.py
```

Run the static analysis tools:

```bash
python -m pylint helpdesk_system.py
python -m bandit -r helpdesk_system.py
python -m flake8 helpdesk_system.py
```

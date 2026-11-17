# Lab 5: Static Code Analysis — IT Helpdesk Ticket Allocator

**Name:** Aadya Arvind  
**SRN:** PES2UG24CS008  
**Section:** 5A CSE  
**Course:** Software Engineering

## Objective
Use Pylint, Bandit, and Flake8 to identify and fix code-quality issues, potential bugs, security vulnerabilities, and formatting problems in the assigned Python IT Helpdesk Ticket Allocator.

## Assigned Problem
**IT Helpdesk Ticket Allocator**

The program supports:
- Creating helpdesk tickets with urgency levels from 1 to 5.
- Assigning tickets to technicians and adding notes.
- Identifying unassigned high-priority tickets.
- Closing tickets after admin password verification.
- Saving ticket information in JSON format.

The admin password is read from the `HELPDESK_ADMIN_PASSWORD` environment variable instead of being stored directly in the source code.

## Static Analysis Tools
- **Pylint:** Checks code quality and programming practices.
- **Bandit:** Identifies potential security vulnerabilities in Python code.
- **Flake8:** Checks Python style and formatting, including PEP 8 issues.

## Issues Addressed
The updated program addresses the following issues:
- **Mutable default argument:** Replaced the shared list default with `None` and initialized the list inside the function.
- **Hard-coded admin password:** Read the password from the `HELPDESK_ADMIN_PASSWORD` environment variable.
- **Unsafe shell execution:** Removed the optional ping functionality that used `subprocess`.
- **Invalid urgency values:** Added validation to accept only integer urgency values from 1 to 5.
- **Missing ticket handling:** Check that a ticket exists before assigning it, adding notes, or closing it.
- **File handling:** Used a context manager and UTF-8 encoding when saving ticket data.
- **Formatting:** Corrected the identified formatting issues.

## Deliverables
- `helpdesk_system.py` — Cleaned and updated IT Helpdesk Ticket Allocator.
- `issues.md` — Table documenting the identified issues and how they were addressed.
- `reflection.md` — Answers to the lab reflection questions.
- `pylint_before.txt` and `pylint_after.txt` — Pylint output files.
- `bandit_before.txt` and `bandit_after.txt` — Bandit output files.
- `flake8_before.txt` and `flake8_after.txt` — Flake8 output files.
- `.gitignore` — Excludes the virtual environment and Python cache files.

## Final Analysis Results
- **Pylint:** **10.00/10**, exceeding the required score of 9.5.
- **Bandit:** The final report records **no issues identified**.
- **Flake8:** The final report file, `flake8_after.txt`, is intentionally empty. Flake8 prints output only when it finds violations, so an empty output file is the expected result when no style issues are reported.

### Note on the Initial Reports
The saved `*_before.txt` files contain the initial command-line messages stating that Pylint, Bandit, and Flake8 were not recognized as commands. They are preserved as recorded, but they are not completed baseline analysis reports. The `*_after.txt` files contain the final analysis output after the tools were run successfully.

## Setup and Execution
Create and activate a virtual environment, then install the analysis tools:

```bash
python -m venv venv
```

Windows Command Prompt:

```cmd
venv\Scripts\activate
```

PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

macOS/Linux:

```bash
source venv/bin/activate
```

Install the tools:

```bash
python -m pip install pylint bandit flake8
```

Set the admin password for the current shell session:

Windows Command Prompt:

```cmd
set HELPDESK_ADMIN_PASSWORD=your_password
```

PowerShell:

```powershell
$env:HELPDESK_ADMIN_PASSWORD="your_password"
```

macOS/Linux:

```bash
export HELPDESK_ADMIN_PASSWORD=your_password
```

Run the program:

```bash
python helpdesk_system.py
```

## Run Static Analysis and Save the Final Reports

Run these commands from the Lab 5 folder:

```bash
python -m pylint helpdesk_system.py > pylint_after.txt 2>&1
python -m bandit -r helpdesk_system.py > bandit_after.txt 2>&1
python -m flake8 helpdesk_system.py > flake8_after.txt 2>&1
```

These commands overwrite the corresponding `*_after.txt` files. A clean Flake8 run produces an empty `flake8_after.txt`; do not add text to that file just to make it non-empty.

# Lab 6: Code and Branch Coverage Analysis — Event Ticket Tier

**Name:** Aadya Arvind  
**SRN:** PES2UG24CS008  
**Section:** 5A CSE  
**Course:** Software Engineering

## Objective
Analyse and improve test coverage for the Event Ticket Tier application using code coverage and branch coverage testing.

## About the Application
The Python application manages event ticket pricing based on seating tiers, order quantities, promotional codes, and exclusive lounge access. It also handles fraudulent booking detection and monitors gate turnstile congestion.

## Test Suites
- `CodeCoverageTest_PES2UG24CS008_application.py` — Test cases for code coverage.
- `BranchCoverageTest_PES2UG24CS008_application.py` — Test cases for branch coverage.
- `test_event_ticket.py` — Original starter test file.

## Deliverables
- `event_ticket_tier.py` — Application module under test.
- `test_event_ticket.py` — Original starter test file.
- `CodeCoverageTest_PES2UG24CS008_application.py` — Code coverage test suite.
- `BranchCoverageTest_PES2UG24CS008_application.py` — Branch coverage test suite.
- `code_coverage.png` — Code coverage terminal report screenshot.
- `branch_coverage.png` — Branch coverage terminal report screenshot.

## Coverage Results
The submitted README reports the following results:

| Coverage Type | Achieved Coverage |
|---|---:|
| Code Coverage | 100% |
| Branch Coverage | 100% |

## Tools Used
- Python 3.12
- pytest
- coverage.py

## Setup and Execution
Install the dependencies:

```bash
pip install pytest coverage
```

Run code coverage:

```bash
py -m coverage erase
py -m coverage run -m pytest CodeCoverageTest_PES2UG24CS008_application.py
py -m coverage report -m
```

Run branch coverage:

```bash
py -m coverage erase
py -m coverage run --branch -m pytest BranchCoverageTest_PES2UG24CS008_application.py
py -m coverage report -m
```


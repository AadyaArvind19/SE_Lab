# Lab 3: Component Modelling & Architectural Pattern Selection

## Student Details
- **Name:** Aadya Arvind
- **SRN:** PES2UG24CS008
- **Section:** 5A CSE

## Objective
To evaluate different architectural styles, select the most appropriate architecture for the assigned system, and create a UML Component Diagram showing components, interfaces and dependencies.

## Problem Statement: Alumni Mentorship & Mock Interview Platform

## Architectural Style Analysis
Evaluated the following architectural styles:
- Layered Architecture
- Microservices Architecture
- Client-Server Architecture

**Selected Architecture:** Layered Architecture

The system is organized into three layers:
- **Presentation Layer:** Handles interaction with students and alumni.
- **Business Layer:** Handles mentor matching, availability, session booking, mock interviews and calendar-related operations.
- **Data Layer:** Stores profiles, mentor slots, sessions and interview scorecards.

## Identified Components
1. Mentorship Portal
2. Session Manager
3. Mock Interview Manager
4. Calendar Connector
5. Platform Database

## Interfaces
- SessionService
- InterviewService
- CalendarService
- SessionData
- ScorecardData
- CalendarData

## Written Justification
Documented the reasons for selecting Layered Architecture, including two scenario-related reasons, a security advantage and a performance benefit.

## Deliverables
1. **UML Component Diagram:** Shows the system components, architectural layers, interfaces and interactions.
2. **Written Justification:** Explains the selected architecture, reasons for selection, security advantage and performance benefit.

## Submitted Files
- `PES2UG24CS008_SE_Lab3.pdf` — Complete lab submission.
- `PES2UG24CS008_Lab3_Diagram.png` — Separately extracted UML Component Diagram.

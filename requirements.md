# Mars Rover Mission Control — Requirements

## Overview
This document defines the Functional and Non-Functional Requirements for the Mars Rover Mission Control system, a software platform that enables remote command and monitoring of Mars exploration rovers over a delayed, bandwidth-limited communication link.

---

## Functional Requirements (FRs)

| ID | Requirement |
|----|-------------|
| FR-01 | The rover shall receive commands from Mission Control and execute valid commands. |
| FR-02 | The rover shall report its current position, battery level, temperature, and communication status. |
| FR-03 | The system shall reject invalid or unauthorized commands. |
| FR-04 |The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level. |
| FR-05 | Mission Control shall receive command execution status. |
| FR-06 | All commands and critical rover events shall be recorded with timestamp and operator ID. |

---

## Non-Functional Requirements (NFRs)

| ID | Requirement | Category |
|----|-------------|----------|
| NFR-01 | The system shall require authenticated and role-authorized operators before accepting rover commands. | Security |
| NFR-02 | The system shall continue operating despite temporary communication interruptions. | Reliability / Availability |
| NFR-03 | Command processing should normally complete within 5 seconds after a command is received by the rover. | Performance |
| NFR-04 | The system shall support at least 20 simultaneously connected rovers. | Scalability |

---

## Notes
- FR-03 (reject invalid/unauthorized commands) and NFR-01 (authentication) overlap conceptually and should be reviewed together during design.
- See `change-requests.md` for the updated versions of FR-04, NFR-04, and NFR-02 following mission scope changes (CR-01, CR-02, CR-03).

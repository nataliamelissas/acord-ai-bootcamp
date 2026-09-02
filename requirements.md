# requirements.md

## Purpose
> Delete this section after reading it.
This document defines the system-level specifications, features, boundary conditions, and acceptance criteria for the project. It outlines exactly what the final product must achieve, anchoring the developer and AI agents to concrete milestones before code implementation begins.

---

## 1. Project Requirements
> Example project requirements, replace with your own
* Define a core system framework for processing calculations.
* Implement basic mathematical functions: addition, subtraction, multiplication, and division.
* Maintain clean state management for tracking the last calculation executed.

## 2. Constraints
> Example project constraints, replace with your own
* All math calculations must strictly return floats.
* Division operations must reject zeros with a clean error message.
* Code must be written using standard language libraries without massive external frameworks.

## 3. Acceptance Criteria (AC)
> Example project AC, replace with at least TWO of your own
### Scenario: Successful Division
* **GIVEN:** The calculation engine is initialized.
* **WHEN:** A request is sent to divide 10 by 2.
* **THEN:** The system returns a value of 5.0.

### Scenario: Zero Division Error
* **GIVEN:** The calculation engine is initialized.
* **WHEN:** A request is sent to divide 10 by 0.
* **THEN:** The system blocks the operation and returns a custom division error.

---

## Condensed Example: Calculator API
> A condensed example of this file. Remember -  being verbose does NOT equal giving good instructions!
* **Example Project Requirements:** Build a lightweight Python Calculator module that saves history to a local text file.
* **Example Constraints:** Do not use third-party math packages; stick entirely to native Python operators.
* **Example Acceptance Criteria:** 
  * **GIVEN:** The history text file is empty.
  * **WHEN:** The student runs an addition of 5.5 and 4.5.
  * **THEN:** The code outputs 10.0 and appends "5.5 + 4.5 = 10.0" directly into the history file.

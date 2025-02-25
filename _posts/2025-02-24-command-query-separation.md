---
layout: post
title:  "Command Query Separation"
---

## Command Query Separation (CQS)

Command Query Separation (CQS) is a principle that helps in structuring applications by separating operations that change state (commands) from those that only retrieve data (queries).

### Commands

Commands modify the system state and involve:

1. **Validate Parameters** – Ensuring inputs meet expected criteria.
2. **Read from Database** – Sometimes necessary for pre-checks.
3. **Perform Action** – Executing business logic.
4. **Write to Database** – Persisting changes.
5. **Log Event** – Tracking changes or actions.
6. **Update View** – Reflecting changes in the UI or API response.

### Queries

Queries do not modify the state and involve:

1. **Validate Parameters** – Ensuring inputs are correct.
2. **Read from Database** – Retrieving required data.
3. **Update View** – Presenting the data.

### Validation

Validation applies to both commands and queries:

1. **Check Values** – Ensuring correctness (e.g., required fields, format).
2. **Check Service and Persistence Constraints** – Ensuring integrity across business rules and database constraints.

### Event Handling

Events help with decoupling components:

1. **Communication Between Components or Endpoints** – Examples include WebSockets, message queues, or APIs exchanging XML/JSON payloads.
2. 

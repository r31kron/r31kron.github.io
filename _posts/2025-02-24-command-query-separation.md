---
layout: post
title:  "Command Query Separation"
---

## Command Query Separation (CQS)

Command Query Separation (CQS) is a principle that helps in structuring applications by separating operations that change state (commands) from those that only retrieve data (queries).

### Commands

Commands modify the system state and involve:

1. **Validate Parameters** – Ensure inputs meet expected criteria.
2. **Read from Database** – Sometimes necessary for pre-checks.
3. **Perform Action** – Execute business logic.
4. **Write to Database** – Persist changes.
5. **Log Event** – Track changes or actions.
6. **Update View** – Reflect changes in UI or API response.

### Queries

Queries do not modify state and involve:

1. **Validate Parameters** – Ensure inputs are correct.
2. **Read from Database** – Retrieve required data.
3. **Update View** – Present the data.

### Validation

Validation applies to both commands and queries:

1. **Check Values** – Ensure correctness (e.g., required fields, format).
2. **Check Service and Persistence Constraints** – Ensure integrity across business rules and database constraints.

### Event Handling

Events help with decoupling components:

1. **Communication Between Components or Endpoints** – Examples include WebSockets, message queues, or APIs exchanging XML/JSON payloads.



---
title: "CIDSD Tickets"
project: "cidsd"
tags:
  - index
  - jira
  - project
---

# CIDSD — Jira Tickets
Total: 112
## Open Tickets
```dataview
TABLE ticket_id, title, status, assignee, created
FROM "Jira Imports"
WHERE project = "cidsd" AND (status != "Closed" AND status != "Done" AND status != "Resolved")
SORT created DESC
```
## All Tickets
```dataview
TABLE ticket_id, title, status, assignee, created
FROM "Jira Imports"
WHERE project = "cidsd"
SORT created DESC
```
---
title: "CITSD Tickets"
project: "citsd"
tags:
  - index
  - jira
  - project
---

# CITSD — Jira Tickets

Total: 863

## Open Tickets
```dataview
TABLE ticket_id, title, status, assignee, created
FROM "Jira Imports"
WHERE project = "citsd" AND (status != "Closed" AND status != "Done" AND status != "Resolved")
SORT created DESC
```

## All Tickets
```dataview
TABLE ticket_id, title, status, assignee, created
FROM "Jira Imports"
WHERE project = "citsd"
SORT created DESC
```


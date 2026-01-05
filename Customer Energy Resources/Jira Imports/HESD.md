---
title: "HESD Tickets"
project: "hesd"
tags:
  - index
  - jira
  - project
---

# HESD — Jira Tickets

Total: 644

## Open Tickets
```dataview
TABLE ticket_id, title, status, assignee, created
FROM "Jira Imports"
WHERE project = "hesd" AND (status != "Closed" AND status != "Done" AND status != "Resolved")
SORT created DESC
```

## All Tickets
```dataview
TABLE ticket_id, title, status, assignee, created
FROM "Jira Imports"
WHERE project = "hesd"
SORT created DESC
```


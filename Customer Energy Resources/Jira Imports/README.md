---
title: "Jira Tickets Index"
created: "2025-12-14 08:22:22"
tags:
  - index
  - jira
  - overview
---

# Jira Tickets Overview

This directory contains 680 tickets converted from JSON exports.

## Dataview Queries

### All Tickets by Status
```dataview
TABLE ticket_id, title, status, assignee, created
FROM "Jira Imports"
SORT status, created DESC
```

### Watchlist Tickets
```dataview
TABLE ticket_id, title, status, assignee, business_impact, created
FROM "Jira Imports"
WHERE contains(tags, "watchlist")
SORT created DESC
```

### Open Tickets
```dataview
TABLE ticket_id, title, assignee, business_impact, created
FROM "Jira Imports"
WHERE status != "Closed" AND status != "Done" AND status != "Resolved"
SORT created DESC
```

### Tickets by Project
```dataview
TABLE ticket_id, title, status, assignee, created
FROM "Jira Imports"
GROUP BY project
SORT project, created DESC
```

### High Impact Tickets
```dataview
TABLE ticket_id, title, status, assignee, business_impact, created
FROM "Jira Imports"
WHERE business_impact = "High" OR business_impact = "Critical"
SORT created DESC
```

### Recent Activity
```dataview
TABLE ticket_id, title, status, scraped_at
FROM "Jira Imports"
SORT scraped_at DESC
LIMIT 20
```

## Statistics

### Tickets by Status
```dataview
TABLE length(rows.ticket_id) as Count
FROM "Jira Imports"
GROUP BY status
SORT Count DESC
```

### Tickets by Project
```dataview
TABLE length(rows.ticket_id) as Count
FROM "Jira Imports"
GROUP BY project
SORT Count DESC
```

---
*Generated on 2025-12-14 08:22:22*

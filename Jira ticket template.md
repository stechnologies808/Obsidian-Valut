---
# Dataview Properties
ticket_id: "{{ticket_id}}"
title: "{{title}}"
status: "{{status}}"
original_status: "{{original_status}}"
created: "{{created}}"
scraped_at: "{{scraped_at}}"
ticket_url: "{{ticket_url}}"
assignee: "{{assignee}}"
reporter: "{{reporter}}"
project: "{{project}}"
request_type: "{{request_type}}"
business_impact: "{{business_impact}}"
business_value: "{{business_value}}"
he_project: "{{he_project}}"
tags:
  - jira
  - ticket
  - {{project_tag}}
  - {{status_slug}}
  {{optional_watchlist}}
updated: "{{updated_ts}}"
last_synced: "{{last_synced_ts}}"
---

# {{ticket_id}}: {{title}}

## Overview
- Status: {{status}}
- Created: {{created_or_Unknown}}
- Project: {{project_or_Unknown}}
- Request Type: {{request_type_or_Unknown}}

## People
- Assignee: {{assignee_or_Unassigned}}
- Reporter: {{reporter_or_Unknown}}

## Business Context
- Business Impact: {{business_impact_or_Not specified}}
- Business Value: {{business_value_or_Not specified}}
- HE Project: {{he_project_or_Not specified}}

## Description
{{description_or_No description available}}

## Comments
{{either a list of comments, or 'No comments available.'}}

## Links
- [View in Jira]({{ticket_url}})
- Original Summary: {{metadata_summary}}

## Metadata
- Scraped: {{scraped_at_or_Unknown}}
- Source: JSON export from Jira Service Management

---
*This file was automatically generated from JSON data*
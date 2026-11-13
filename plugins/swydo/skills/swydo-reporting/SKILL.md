---
name: swydo-reporting
description: Answer questions about Swydo clients, reports, monitoring boards, alerts, goals and marketing performance data using the Swydo MCP server. Use when the user asks about their agency's clients, campaign performance, or Swydo reports.
---

# Swydo reporting

## When to use

- The user asks how a client's campaigns, ads or keywords perform
- The user asks about Swydo reports, monitoring boards, alerts or goals
- The user wants to compare marketing data across data sources or periods

## Instructions

1. Start with `list_teams` when the user belongs to more than one team, then `list_clients` to find the client.
2. Before advising on a client, check its client rules and past decisions. Respect rules such as "Never run brand campaigns".
3. To fetch metrics, find the data source with `list_data_sources`, the report type with `list_categories`, and the metrics and dimensions with `list_fields`. Check `get_field_compatibility` before combining fields, then call `get_data_source_data`.
4. For existing work, use `list_reports`, `list_boards`, `list_monitoring_views`, `list_alerts` and `list_goals`, and their `get_*` counterparts for details.
5. State the date range and data source behind every number you report.
6. When an error says what to change, change the request and retry. When it says to reconnect, reauthorize or contact support, stop and tell the user.

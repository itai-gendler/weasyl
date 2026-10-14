---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator opens a report",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "report",
          "effect": "reads",
          "facts": [
            "Reported item",
            "Violation",
            "Report comments",
            "Assigned moderator",
            "Opened at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::report"
        }
      }
    }
  ]
}
---

# Open a report

## Trigger

A moderator picks a report.

## Outcome

The moderator sees the item, comments and the owner's blocked-tag matches.

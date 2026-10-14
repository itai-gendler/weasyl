---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator chooses Close: no action taken and writes an explanation",
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
    },
    {
      "text": "The Product closes the report",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "report",
          "effect": "changes",
          "from": "Under review",
          "to": "Closed",
          "facts": [
            "Assigned moderator",
            "Closure reason",
            "Closure explanation"
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

# Close a report with no action taken

## Trigger

A moderator finds nothing wrong.

## Outcome

The report is closed with its reason and explanation.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator chooses Unassign from me on a report",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "report",
          "effect": "reads",
          "facts": [
            "Assigned moderator"
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
      "text": "The Product returns the report to open",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "report",
          "effect": "changes",
          "from": "Under review",
          "to": "Open",
          "facts": [
            "Assigned moderator"
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

# Unassign a report

## Trigger

A moderator cannot finish a report.

## Outcome

The report is open again for anyone.

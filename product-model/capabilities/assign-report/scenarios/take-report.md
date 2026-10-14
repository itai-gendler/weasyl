---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator chooses Assign to me on a report",
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
      "text": "The Product puts the report under review by the moderator",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "report",
          "effect": "changes",
          "from": "Open",
          "to": "Under review",
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

# Assign a report to oneself

## Trigger

A moderator takes responsibility for a report.

## Outcome

The report is under review by the moderator.

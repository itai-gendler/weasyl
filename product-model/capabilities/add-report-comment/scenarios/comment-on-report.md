---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator writes a remark on a report",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "report",
          "effect": "reads",
          "facts": [
            "Report comments"
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
      "text": "The Product adds the remark to the report",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "report",
          "effect": "changes",
          "facts": [
            "Report comments"
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

# Add a comment to a report

## Trigger

A moderator wants to leave context for other staff.

## Outcome

The comment shows among the report comments.

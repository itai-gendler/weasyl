---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator opens the reported content list",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "report",
          "effect": "reads",
          "facts": [
            "Reported item",
            "Violation",
            "Assigned moderator",
            "Opened at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::reports"
        }
      }
    }
  ]
}
---

# List open reports

## Trigger

A moderator starts handling reports.

## Outcome

The moderator sees open reports, newest first, with their violations and reporter counts.

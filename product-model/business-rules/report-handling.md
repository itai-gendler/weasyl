---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "report",
      "effect": "changes",
      "to": "Under review"
    },
    {
      "type": "entity",
      "id": "report",
      "effect": "changes",
      "to": "Open"
    },
    {
      "type": "entity",
      "id": "report",
      "effect": "changes",
      "to": "Closed"
    }
  ],
  "permits": [
    {
      "actors": [
        "moderator",
        "administrator",
        "director"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/report.py#close"
    }
  ]
}
---

# Only staff assign, unassign and close reports

Reporters cannot change a report's status after filing it.

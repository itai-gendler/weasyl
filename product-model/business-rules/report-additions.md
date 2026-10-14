---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "report",
      "effect": "changes",
      "facts": [
        "Violation",
        "Report comments"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "member"
      ]
    },
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
      "target": "weasyl/report.py#create"
    }
  ]
}
---

# Members add reports to an open report and staff add remarks

Each addition keeps who wrote it and when.

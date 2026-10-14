---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "report",
      "effect": "reads"
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
      "target": "weasyl/report.py#select_list"
    }
  ]
}
---

# Only staff see reports

Reporters see only that they reported an item.

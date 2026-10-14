---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "submission",
      "effect": "changes",
      "to": "Visible"
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
      "target": "weasyl/moderation.py#bulk_edit"
    }
  ]
}
---

# Only staff make hidden submissions visible again

Owners cannot undo a removal themselves.

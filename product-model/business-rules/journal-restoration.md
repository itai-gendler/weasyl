---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "journal",
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

# Only staff make hidden journals visible again

Owners cannot undo a removal themselves.

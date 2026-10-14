---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "submission",
      "effect": "changes",
      "to": "Hidden"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "owns",
          "entity": "account"
        },
        {
          "verb": "holds",
          "entity": "member"
        }
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
      "target": "weasyl/submission.py#remove"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/moderation.py#bulk_edit"
    }
  ]
}
---

# Only the owner or staff hide submissions

Removing is hiding: nothing is erased, and staff can still see and restore it.

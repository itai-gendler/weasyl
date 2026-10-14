---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "character",
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
      "target": "weasyl/character.py#remove"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/moderation.py#bulk_edit"
    }
  ]
}
---

# Only the owner or staff hide characters

Removing is hiding: nothing is erased, and staff can still see and restore it.

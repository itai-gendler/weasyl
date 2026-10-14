---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "shout",
      "effect": "changes",
      "to": "Hidden"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "writes",
          "entity": "account"
        },
        {
          "verb": "holds",
          "entity": "member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "receives",
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
      "target": "weasyl/shout.py#remove"
    }
  ]
}
---

# The profile owner, staff, or the writer of a shout without replies hide a shout

Hidden shouts stay visible to staff.

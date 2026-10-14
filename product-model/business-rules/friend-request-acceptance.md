---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "friendship",
      "effect": "changes",
      "to": "Accepted"
    }
  ],
  "permits": [
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
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/frienduser.py#request"
    }
  ]
}
---

# Only the recipient accepts a friend request

The sender cannot accept their own request.

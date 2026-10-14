---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "collection",
      "effect": "changes",
      "from": "Requested",
      "to": "Accepted"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "is collected as",
          "entity": "submission"
        },
        {
          "verb": "owns",
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
      "target": "weasyl/collection.py#pending_accept"
    }
  ]
}
---

# Only the artist accepts a collection request

The requester cannot accept their own request.

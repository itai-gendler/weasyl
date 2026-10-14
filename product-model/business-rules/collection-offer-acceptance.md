---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "collection",
      "effect": "changes",
      "from": "Offered",
      "to": "Accepted"
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

# Only the collector accepts a collection offer

The artist cannot accept on the collector's behalf.

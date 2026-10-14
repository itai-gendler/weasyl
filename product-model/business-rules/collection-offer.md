---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "collection",
      "effect": "creates",
      "to": "Offered"
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
      "target": "weasyl/collection.py#offer"
    }
  ]
}
---

# Only the artist offers a submission as a collection

Friends-only submissions cannot be collected, and neither member may ignore the other.

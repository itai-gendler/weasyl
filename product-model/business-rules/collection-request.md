---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "collection",
      "effect": "creates",
      "to": "Requested"
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
      ],
      "when": [
        {
          "entity": "account",
          "fact": "Verification",
          "is": "Verified"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/collection.py#request"
    }
  ]
}
---

# Only verified members request a collection, where the artist allows requests

The submission must be within the requester's rating and not friends only, and a requester may have at most ten requests pending with one artist.

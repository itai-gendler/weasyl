---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "collection",
      "effect": "removes"
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
      "target": "weasyl/collection.py#pending_reject"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/collection.py#remove"
    }
  ]
}
---

# The collector rejects offers and removes collections; the artist rejects requests

An accepted collection is removed only by its collector.

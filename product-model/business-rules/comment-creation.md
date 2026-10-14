---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "comment",
      "effect": "creates"
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
      "target": "weasyl/comment.py#insert"
    }
  ]
}
---

# Only verified members comment

They comment only on items they can see, and not where the owner, or the writer replied to, ignores them or is ignored by them.

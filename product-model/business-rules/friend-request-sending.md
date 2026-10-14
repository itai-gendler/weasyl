---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "friendship",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "sends",
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
      "target": "weasyl/frienduser.py#request"
    }
  ]
}
---

# Only verified members send friend requests

Neither member may ignore the other.

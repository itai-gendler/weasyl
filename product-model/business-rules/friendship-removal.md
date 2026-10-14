---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "friendship",
      "effect": "removes"
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
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/frienduser.py#remove"
    }
  ]
}
---

# Either member ends a friendship or friend request

Either side may also end it by ignoring the other.

---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "follow",
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
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/followuser.py#remove"
    }
  ]
}
---

# Only the follower ends a follow

The followed member cannot remove a follower, except by ignoring them.

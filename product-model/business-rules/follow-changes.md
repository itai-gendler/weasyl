---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "follow",
      "effect": "changes"
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
      "target": "weasyl/followuser.py#update"
    }
  ]
}
---

# Only the follower changes what a follow notifies about

The followed member cannot see or change it.

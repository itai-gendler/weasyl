---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "follow",
      "effect": "creates"
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
      "target": "weasyl/followuser.py#insert"
    }
  ]
}
---

# Only the follower follows, changes or ends a follow

Neither member may ignore the other when following starts.

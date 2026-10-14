---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "favorite",
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
      "target": "weasyl/favorite.py#insert"
    }
  ]
}
---

# Members favorite other people's posts, never their own

Neither member may ignore the other, and friends-only posts may be favorited only by friends.

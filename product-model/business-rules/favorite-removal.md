---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "favorite",
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
      "target": "weasyl/favorite.py#remove"
    }
  ]
}
---

# Only the member who favorited removes the favorite

Nobody else can take a member's favorite away.

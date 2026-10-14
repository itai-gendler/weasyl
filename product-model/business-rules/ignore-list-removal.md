---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "ignore-list-entry",
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
      "target": "weasyl/ignoreuser.py#remove"
    }
  ]
}
---

# Only the member takes someone off their ignore list

The ignored member cannot remove themself from the list.

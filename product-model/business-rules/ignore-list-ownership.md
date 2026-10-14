---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "ignore-list-entry",
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
      "target": "weasyl/ignoreuser.py#insert"
    }
  ]
}
---

# Only the member keeps their ignore list, and staff cannot be ignored

Nobody can ignore a moderator, administrator or director, or themself.

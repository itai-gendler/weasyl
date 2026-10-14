---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Username"
      ]
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "holds",
          "entity": "member"
        }
      ]
    },
    {
      "actors": [
        "administrator",
        "director"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/login.py#change_username"
    }
  ]
}
---

# Only the account holder or an administrator changes a username

A holder may change to a new name once every 30 days; a change of capitalization alone does not count. Administrators are not held to the limit. A new name must not be held by any account, pending sign-up, alias or former name still in use.

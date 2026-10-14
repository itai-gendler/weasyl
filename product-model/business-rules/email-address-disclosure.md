---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "reads",
      "facts": [
        "Email address"
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
      "target": "weasyl/moderation.py#finduser"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/profile.py#select_manage"
    }
  ]
}
---

# Only the account holder and administrators see an account's email address

Administrators see it when managing or searching accounts.

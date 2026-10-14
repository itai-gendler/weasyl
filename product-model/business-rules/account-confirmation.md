---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "from": "Unconfirmed",
      "to": "Active"
    }
  ],
  "permits": [
    {
      "actors": [
        "visitor"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/login.py#verify"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/login.py#_delete_expired"
    }
  ]
}
---

# An account becomes active only from its emailed confirmation link

The confirmation link works within two days of sign-up; afterwards the sign-up lapses and must be repeated.

---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "to": "Suspended"
    },
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "to": "Banned"
    },
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "from": "Banned",
      "to": "Active"
    }
  ],
  "permits": [
    {
      "actors": [
        "moderator",
        "administrator",
        "director"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/moderation.py#setusermode"
    }
  ]
}
---

# Only staff suspend, ban or release accounts, and never another staff member

Suspending, banning and releasing are refused when the account belongs to a moderator, administrator or director.

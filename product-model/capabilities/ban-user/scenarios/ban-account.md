---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator enters a username and a reason and chooses Permanently Ban User",
      "kind": "actor",
      "actor": "moderator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::staff::user-suspensions"
        }
      }
    },
    {
      "text": "The Product bans the account and adds a staff note",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "from": "Active",
          "to": "Banned",
          "facts": [
            "Ban reason"
          ]
        },
        {
          "entity": "staff-note",
          "effect": "creates",
          "facts": [
            "Content",
            "Written at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::user-suspensions"
        }
      }
    }
  ]
}
---

# Ban an account

## Trigger

A moderator decides an account must leave for good.

## Outcome

The account can never sign in, and its staff notes record why.

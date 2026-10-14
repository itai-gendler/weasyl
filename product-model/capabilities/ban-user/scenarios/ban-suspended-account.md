---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator enters the username of a suspended account and a reason and chooses Permanently Ban User",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::user-suspensions"
        }
      }
    },
    {
      "text": "The Product replaces the suspension of the account with a ban and adds a staff note",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "from": "Suspended",
          "to": "Banned",
          "facts": [
            "Suspension",
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

# Ban a suspended account

## Trigger

A moderator bans an account already suspended.

## Outcome

The suspension is replaced by the ban.

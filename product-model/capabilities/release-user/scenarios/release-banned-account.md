---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator enters the username of a banned account and chooses Release User",
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
      "text": "The Product lifts the ban of the account and adds a staff note",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "from": "Banned",
          "to": "Active",
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

# Release a banned account

## Trigger

Staff reverse a ban.

## Outcome

The account can sign in again.

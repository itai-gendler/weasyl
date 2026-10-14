---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator enters the username of a suspended account and chooses Release User",
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
      "text": "The Product lifts the suspension of the account and adds a staff note",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "from": "Suspended",
          "to": "Active",
          "facts": [
            "Suspension"
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

# Release a suspended account

## Trigger

A moderator ends a suspension early.

## Outcome

The account can sign in again.

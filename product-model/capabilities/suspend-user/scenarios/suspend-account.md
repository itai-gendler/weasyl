---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator enters a username, a reason and a duration or release date and chooses Temporarily Suspend User",
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
      "text": "The Product suspends the account until the release date and adds a staff note",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "from": "Active",
          "to": "Suspended",
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

# Suspend an account

## Trigger

A moderator decides an account needs a break.

## Outcome

The account cannot sign in until the release date, and its staff notes record why.

## Edge cases

- A release date that is not in the future is refused.

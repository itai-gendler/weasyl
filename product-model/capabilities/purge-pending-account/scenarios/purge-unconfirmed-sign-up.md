---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator opens the accounts pending creation and purges one",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Username",
            "Email address"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::pending-accounts"
        }
      }
    },
    {
      "text": "The Product removes the unconfirmed account",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "account",
          "effect": "removes",
          "from": "Unconfirmed"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::pending-accounts"
        }
      }
    }
  ]
}
---

# Purge a pending account

## Trigger

A sign-up is stuck or abusive.

## Outcome

The pending account is gone and its link no longer works.

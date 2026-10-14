---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator opens an account, ticks the details to change and enters them",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Username",
            "Full name",
            "Catchphrase",
            "Birthday",
            "Profile details",
            "Tag suggestions allowed"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::account-management"
        }
      }
    },
    {
      "text": "The Product saves the chosen details of the account",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Username",
            "Full name",
            "Catchphrase",
            "Birthday",
            "Profile details",
            "Tag suggestions allowed"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::account-management"
        }
      }
    }
  ]
}
---

# Correct account details

## Trigger

An administrator needs to fix an account, such as recording a birthday.

## Outcome

The account has the corrected details.

## Edge cases

- A username changed here is not held to the 30-day limit.

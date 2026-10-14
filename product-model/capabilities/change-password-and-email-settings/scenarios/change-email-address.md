---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters their current password and a new email address",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Email address"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::password-and-email"
        }
      }
    },
    {
      "text": "The Product emails a confirmation link to the new address",
      "kind": "product",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::password-and-email"
        }
      }
    },
    {
      "text": "The Member opens the confirmation link while signed in",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community"
        }
      }
    },
    {
      "text": "The Product changes the email address of the account",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Email address"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community"
        }
      }
    }
  ]
}
---

# Change email address

## Trigger

A member wants account email at a new address.

## Outcome

The account uses the new address once its confirmation link is followed.

## Edge cases

- When the new address belongs to another account, that address is told so and nothing changes.

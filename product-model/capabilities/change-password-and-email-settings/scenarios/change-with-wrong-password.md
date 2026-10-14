---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a wrong current password and a new password",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::password-and-email"
        }
      }
    },
    {
      "text": "The current password does not match the account",
      "kind": "condition",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Password"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::password-and-email"
        }
      }
    }
  ]
}
---

# Change with a wrong current password

## Trigger

A member enters the wrong current password.

## Outcome

Neither the password nor the email address changes.

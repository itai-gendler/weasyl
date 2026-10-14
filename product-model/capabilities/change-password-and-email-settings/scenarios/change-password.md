---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters their current password and a new password",
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
      "text": "The Product sets the new password on the account and ends its other sessions",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Password"
          ]
        },
        {
          "entity": "session",
          "effect": "removes"
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

# Change password

## Trigger

A member wants a new password.

## Outcome

The new password is in effect and other sessions are signed out.

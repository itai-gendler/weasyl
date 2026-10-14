---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member confirms their password, scans the code into an authenticator app, saves the recovery codes and enters a current code",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::two-factor-authentication"
        }
      }
    },
    {
      "text": "The Product turns on two-factor authentication for the account with the saved recovery codes",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Two-factor authentication"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::two-factor-authentication"
        }
      }
    }
  ]
}
---

# Turn on two-factor authentication

## Trigger

A member wants a second factor at sign-in.

## Outcome

Sign-in asks for an authenticator or recovery code from now on.

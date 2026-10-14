---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor enters their username and password, optionally choosing SFW mode",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The password matches and the account is not suspended, banned or using two-factor authentication",
      "kind": "condition",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Password",
            "Two-factor authentication"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    },
    {
      "text": "The Product starts a session for the account",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "session",
          "effect": "creates",
          "facts": [
            "SFW mode",
            "Signed in at"
          ]
        },
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-in"
        }
      }
    }
  ]
}
---

# Sign in with username and password

## Trigger

A visitor wants to use their account.

## Outcome

The person is signed in and returned to the page they came from.

## Edge cases

- Credentials a protecting proxy reports as leaked are refused even when correct.
- A former username is not accepted, and the error hints that the username may have changed.

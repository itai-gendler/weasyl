---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor enters their username and password",
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
      "text": "The password matches and the account uses two-factor authentication",
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
      "text": "The Visitor enters an authenticator code or a recovery code within five minutes",
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

# Sign in with a second factor

## Trigger

A person whose account uses two-factor authentication signs in.

## Outcome

The person is signed in after giving a valid code.

## Edge cases

- After five wrong codes, or after five minutes, the person must start again with their password.
- Using the last recovery code signs the person in and turns two-factor authentication off.

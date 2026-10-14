---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor enters a username, email address and password",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::sign-up"
        }
      }
    },
    {
      "text": "The email address already belongs to an account or a pending sign-up",
      "kind": "condition",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-up"
        }
      }
    },
    {
      "text": "The Product emails the address the username of the existing account instead of a confirmation link",
      "kind": "product",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Username"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-up"
        }
      }
    }
  ]
}
---

# Sign up with an email address already in use

## Trigger

A visitor signs up with an email address an account already uses.

## Outcome

The visitor sees the usual success message, and the mailbox owner learns which account already uses the address; no new account can be confirmed.

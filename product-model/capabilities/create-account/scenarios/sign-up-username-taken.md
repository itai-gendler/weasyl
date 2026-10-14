---
{
  "kind": "validation",
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
      "text": "The username belongs to an account, a pending sign-up, an alias or a former username still pointing to its account",
      "kind": "condition",
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

# Sign up with a username already in use

## Trigger

A visitor signs up with a username someone already holds.

## Outcome

Nothing is reserved and the visitor is asked for another username.

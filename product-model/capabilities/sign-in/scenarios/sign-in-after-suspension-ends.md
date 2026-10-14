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
      "text": "The release date of the account's suspension has passed",
      "kind": "condition",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Suspension"
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
      "text": "The Product lifts the suspension of the account and starts a session",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "from": "Suspended",
          "to": "Active",
          "facts": [
            "Suspension"
          ]
        },
        {
          "entity": "session",
          "effect": "creates",
          "facts": [
            "SFW mode",
            "Signed in at"
          ]
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

# Sign in after a suspension ends

## Trigger

A suspended person signs in after the release date.

## Outcome

The suspension is lifted and the person is signed in.

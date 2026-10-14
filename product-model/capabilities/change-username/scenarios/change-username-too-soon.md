---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a new username",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::username-settings"
        }
      }
    },
    {
      "text": "The account changed its username less than 30 days ago",
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
          "place": "web::community::username-settings"
        }
      }
    }
  ]
}
---

# Change username again within 30 days

## Trigger

A member changed their username less than 30 days ago.

## Outcome

The username is unchanged and the member is told to wait.

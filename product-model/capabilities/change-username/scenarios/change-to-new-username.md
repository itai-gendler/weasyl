---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a new username",
      "kind": "actor",
      "actor": "member",
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
    },
    {
      "text": "The Product changes the username of the account and keeps the former name pointing to it",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
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

# Change username

## Trigger

A member wants a different username.

## Outcome

The profile and sign-in use the new name and links with the former name still lead to the member.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator opens an account in user management and removes its avatar",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Username",
            "Avatar"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::user-management"
        }
      }
    },
    {
      "text": "The Product removes the avatar of the account and adds a staff note",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Avatar"
          ]
        },
        {
          "entity": "staff-note",
          "effect": "creates",
          "facts": [
            "Content",
            "Written at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::user-management"
        }
      }
    }
  ]
}
---

# Remove an avatar

## Trigger

A moderator finds an inappropriate avatar.

## Outcome

The account shows the default avatar.

## Edge cases

- The banner is removed the same way.

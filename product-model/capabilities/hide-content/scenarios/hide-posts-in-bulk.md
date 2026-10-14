---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator selects journals among the content of an account and chooses Hide",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "journal",
          "effect": "reads",
          "facts": [
            "Title"
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
          "place": "web::staff::user-content"
        }
      }
    },
    {
      "text": "The Product changes the journals to hidden and adds a staff note listing them",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "journal",
          "effect": "changes",
          "from": "Visible",
          "to": "Hidden",
          "facts": []
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
          "place": "web::staff::user-content"
        }
      }
    }
  ]
}
---

# Hide several posts of an account

## Trigger

A moderator reviews everything one account posted.

## Outcome

The chosen posts are hidden and the owner's staff notes list them.

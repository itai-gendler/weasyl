---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator selects journals among the content of an account and chooses Show",
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
      "text": "The Product changes the journals to visible and adds a staff note listing them",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "journal",
          "effect": "changes",
          "from": "Hidden",
          "to": "Visible",
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

# Show several posts of an account

## Trigger

A moderator reviews everything one account posted.

## Outcome

The chosen posts are shown and the owner's staff notes list them.

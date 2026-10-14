---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses to remove their character and confirms",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::character-page"
        }
      }
    },
    {
      "text": "The Product hides the character and removes the notifications about it",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
          "effect": "changes",
          "from": "Visible",
          "to": "Hidden",
          "facts": []
        },
        {
          "entity": "notification",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::character-page"
        }
      }
    }
  ]
}
---

# Remove a character

## Trigger

An owner no longer wants a character shown.

## Outcome

The character is gone from the profile and notifications.

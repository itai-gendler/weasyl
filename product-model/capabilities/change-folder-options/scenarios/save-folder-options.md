---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses the options of a folder and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "folder",
          "effect": "reads",
          "facts": [
            "Featured",
            "Hidden from front page",
            "Hidden from profile",
            "No follower notifications"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::folder-options"
        }
      }
    },
    {
      "text": "The Product saves the options of the folder",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "folder",
          "effect": "changes",
          "facts": [
            "Featured",
            "Hidden from front page",
            "Hidden from profile",
            "No follower notifications"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::folder-options"
        }
      }
    }
  ]
}
---

# Save folder options

## Trigger

A member wants a folder to behave differently.

## Outcome

The folder's submissions follow the new options.

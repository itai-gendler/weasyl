---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects the area of the character image to use",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
          "effect": "reads",
          "facts": [
            "Thumbnail"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::thumbnail-selection"
        }
      }
    },
    {
      "text": "The Product saves the thumbnail of the character",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
          "effect": "changes",
          "facts": [
            "Thumbnail"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::thumbnail-selection"
        }
      }
    }
  ]
}
---

# Crop a character thumbnail

## Trigger

An owner selects the thumbnail of their character.

## Outcome

Galleries show the new thumbnail and the owner is on the character.

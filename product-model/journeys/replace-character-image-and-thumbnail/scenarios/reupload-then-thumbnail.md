---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses a new image for their character",
      "kind": "actor",
      "actor": "member",
      "capability": "reupload-character-image",
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
          "place": "web::community::file-reupload"
        }
      }
    },
    {
      "text": "The Product replaces the image of the character and takes the Member to select its thumbnail",
      "kind": "product",
      "actor": "member",
      "capability": "reupload-character-image",
      "entities": [
        {
          "entity": "character",
          "effect": "changes",
          "facts": [
            "Image"
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
      "text": "The Member selects the area of the image to use",
      "kind": "actor",
      "actor": "member",
      "capability": "select-thumbnail",
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
      "capability": "select-thumbnail",
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

# Reupload a character image, then select its thumbnail

## Trigger

An owner has a new image for a character.

## Outcome

The character shows the new image and thumbnail.

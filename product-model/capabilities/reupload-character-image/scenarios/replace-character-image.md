---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses a new image for their character",
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
          "place": "web::community::file-reupload"
        }
      }
    },
    {
      "text": "The Product replaces the image of the character",
      "kind": "product",
      "actor": "member",
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
          "place": "web::community::file-reupload"
        }
      }
    },
    {
      "text": "The Product takes the Member to select the thumbnail of the character",
      "kind": "product",
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
    }
  ]
}
---

# Replace a character image

## Trigger

An owner has a new reference image.

## Outcome

The character shows the new image and the owner is selecting its thumbnail.

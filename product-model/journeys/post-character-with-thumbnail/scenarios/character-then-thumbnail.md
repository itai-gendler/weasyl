---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member uploads the character image and enters its details",
      "kind": "actor",
      "actor": "member",
      "capability": "submit-character",
      "entities": [
        {
          "entity": "character",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::character-form"
        }
      }
    },
    {
      "text": "The Product creates the character and takes the Member to select its thumbnail",
      "kind": "product",
      "actor": "member",
      "capability": "submit-character",
      "entities": [
        {
          "entity": "character",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Name",
            "Age",
            "Gender",
            "Height",
            "Weight",
            "Species",
            "Description",
            "Rating",
            "Tags",
            "Friends only",
            "Image",
            "Posted at"
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

# Submit a character, then select its thumbnail

## Trigger

A verified member submits a character.

## Outcome

The character is posted with the chosen thumbnail and the member is on its page.

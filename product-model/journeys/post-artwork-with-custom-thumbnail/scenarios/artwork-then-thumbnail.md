---
{
  "kind": "primary",
  "result": "achieved",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member uploads an image, enters its details and asks to choose a custom thumbnail",
      "kind": "actor",
      "actor": "member",
      "capability": "submit-artwork",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::artwork-form"
        }
      }
    },
    {
      "text": "The Product creates the submission and takes the Member to select its thumbnail",
      "kind": "product",
      "actor": "member",
      "capability": "submit-artwork",
      "entities": [
        {
          "entity": "submission",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Title",
            "Description",
            "Category",
            "Rating",
            "Folder",
            "Tags",
            "Friends only",
            "Critique requested",
            "Submission file",
            "Cover art",
            "Thumbnail",
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
          "entity": "submission",
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
      "text": "The Product saves the thumbnail of the submission",
      "kind": "product",
      "actor": "member",
      "capability": "select-thumbnail",
      "entities": [
        {
          "entity": "submission",
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

# Submit artwork, then select its thumbnail

## Trigger

A verified member submits a picture and asks to choose its thumbnail.

## Outcome

The submission is posted with the chosen thumbnail and the member is on its page.

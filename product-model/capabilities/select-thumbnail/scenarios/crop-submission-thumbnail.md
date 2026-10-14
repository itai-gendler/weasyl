---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects the area of the image to use",
      "kind": "actor",
      "actor": "member",
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

# Crop a submission thumbnail

## Trigger

An owner wants a better gallery thumbnail.

## Outcome

Galleries show the new thumbnail and the owner is back on the submission.

## Edge cases

- Uploading a separate image instead keeps the member on the page to crop it.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member changes the details of their submission and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Description",
            "Category",
            "Rating",
            "Folder",
            "Friends only",
            "Critique requested"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-details-form"
        }
      }
    },
    {
      "text": "The Product saves the details of the submission",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "changes",
          "facts": [
            "Title",
            "Description",
            "Category",
            "Rating",
            "Folder",
            "Friends only",
            "Critique requested"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-details-form"
        }
      }
    }
  ]
}
---

# Edit submission details

## Trigger

An owner wants to correct or update a submission.

## Outcome

The submission shows the new details.

## Edge cases

- The category stays the same; only the subcategory within it changes.

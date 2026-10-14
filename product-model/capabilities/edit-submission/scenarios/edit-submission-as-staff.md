---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator changes the details of a member's submission and saves",
      "kind": "actor",
      "actor": "moderator",
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
        },
        {
          "entity": "member",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-details-form"
        }
      }
    },
    {
      "text": "The Product saves the details of the submission and adds a staff note about the edit",
      "kind": "product",
      "actor": "moderator",
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
          "place": "web::community::submission-details-form"
        }
      }
    }
  ]
}
---

# Edit a submission as staff

## Trigger

A moderator corrects a member's submission.

## Outcome

The submission shows the new details and the owner's staff notes record the edit.

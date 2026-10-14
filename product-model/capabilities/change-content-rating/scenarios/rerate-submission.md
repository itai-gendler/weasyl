---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator chooses Rate explicit under Submission Moderation",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Rating"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-page"
        }
      }
    },
    {
      "text": "The Product changes the rating of the submission and adds a staff note listing the change",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "submission",
          "effect": "changes",
          "facts": [
            "Rating"
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
          "place": "web::community::submission-page"
        }
      }
    }
  ]
}
---

# Re-rate a submission from its page

## Trigger

A moderator finds a submission rated too low.

## Outcome

The submission has the new rating and the owner's staff notes list the change.

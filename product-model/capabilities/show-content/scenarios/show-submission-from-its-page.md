---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator chooses Show under Submission Moderation on a member's submission",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title"
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
          "place": "web::community::submission-page"
        }
      }
    },
    {
      "text": "The Product changes the submission to visible and adds a staff note listing it",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "submission",
          "effect": "changes",
          "from": "Hidden",
          "to": "Visible",
          "facts": []
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

# Show a submission from its page

## Trigger

A moderator decides a member's submission should be shown.

## Outcome

The submission is shown and the owner's staff notes list it.

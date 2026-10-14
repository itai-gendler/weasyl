---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator chooses Hide under Submission Moderation on a member's submission",
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
      "text": "The Product changes the submission to hidden and adds a staff note listing it",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "submission",
          "effect": "changes",
          "from": "Visible",
          "to": "Hidden",
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

# Hide a submission from its page

## Trigger

A moderator decides a member's submission should be hidden.

## Outcome

The submission is hidden and the owner's staff notes list it.

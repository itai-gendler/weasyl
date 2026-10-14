---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member writes a comment on a submission",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        },
        {
          "entity": "comment",
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
      "text": "The Product posts the comment and notifies the owner of the submission and its collectors",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "comment",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Content",
            "Posted at"
          ]
        },
        {
          "entity": "notification",
          "effect": "creates",
          "facts": [
            "Kind",
            "Sender",
            "Subject",
            "Received at"
          ]
        },
        {
          "entity": "submission",
          "effect": "reads",
          "facts": []
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

# Comment on a submission

## Trigger

A verified member wants to respond to a submission.

## Outcome

The comment shows under the submission and its owner is notified.

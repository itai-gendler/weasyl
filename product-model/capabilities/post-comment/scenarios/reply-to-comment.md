---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member writes a reply to a comment on a journal",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "comment",
          "effect": "reads",
          "facts": [
            "Content"
          ]
        },
        {
          "entity": "journal",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::journal-page"
        }
      }
    },
    {
      "text": "The Product posts the reply comment and notifies the writer of the replied-to comment",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "comment",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Content",
            "Posted at",
            "Reply to"
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
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::journal-page"
        }
      }
    }
  ]
}
---

# Reply to a comment

## Trigger

A verified member answers someone's comment.

## Outcome

The reply shows beneath the comment and its writer is notified.

## Edge cases

- Replying to a hidden comment is allowed.

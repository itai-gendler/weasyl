---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member writes a comment on a site update",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "site-update",
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
          "place": "web::community::site-update"
        }
      }
    },
    {
      "text": "The Product posts the comment and notifies the staff member who posted the update",
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
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::site-update"
        }
      }
    }
  ]
}
---

# Comment on a site update

## Trigger

A verified member responds to staff news.

## Outcome

The comment shows under the site update.

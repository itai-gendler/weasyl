---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a published Google Docs link, a title, category, rating and tags",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::artwork-form"
        }
      }
    },
    {
      "text": "The Product creates the literary submission embedding the document",
      "kind": "product",
      "actor": "member",
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
            "Embedded media",
            "Cover art",
            "Thumbnail",
            "Posted at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::artwork-form"
        }
      }
    },
    {
      "text": "The Product notifies each follower whose Follow covers submissions, whose rating preference allows it and who does not block its tags",
      "kind": "product",
      "entities": [
        {
          "entity": "follow",
          "effect": "reads",
          "facts": [
            "Notification kinds"
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
          "place": "web::community::artwork-form"
        }
      }
    },
    {
      "text": "The new submission is shown on its page",
      "kind": "condition",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Embedded media"
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

# Submit writing embedded from Google Docs

## Trigger

A verified member wants to share a story published in Google Docs.

## Outcome

The submission shows the embedded document.

## Edge cases

- A link that is not a published Google Docs document is refused.

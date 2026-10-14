---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens their submission notifications",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "notification",
          "effect": "reads",
          "facts": [
            "Sender",
            "Received at"
          ]
        },
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Thumbnail"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-notifications"
        }
      }
    }
  ]
}
---

# Review new submissions

## Trigger

A member wants to catch up on the people they follow.

## Outcome

The member sees the new work as thumbnails, newest first.

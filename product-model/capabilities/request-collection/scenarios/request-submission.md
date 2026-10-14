---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Request This Submission",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title"
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
      "text": "The Product creates the collection request and notifies the artist",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "collection",
          "effect": "creates",
          "to": "Requested",
          "facts": [
            "Collected at"
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
          "place": "web::community::submission-page"
        }
      }
    }
  ]
}
---

# Request a submission for collections

## Trigger

A member wants a piece made for or featuring them in their gallery.

## Outcome

The artist has a pending collection request.

---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member marks their submission friends only and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Friends only"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-details-form"
        }
      }
    },
    {
      "text": "The Product saves the submission as friends only and removes its notifications from members who are not friends",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "changes",
          "facts": [
            "Friends only"
          ]
        },
        {
          "entity": "notification",
          "effect": "removes"
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

# Make a submission friends only

## Trigger

An owner limits an existing submission to friends.

## Outcome

Notifications about it disappear for everyone who is not a friend.

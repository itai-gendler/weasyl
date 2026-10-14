---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens a friends-only submission",
      "kind": "actor",
      "actor": "member",
      "entities": [
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
    },
    {
      "text": "The submission is friends only and the member is not a friend of its owner",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Friends only"
          ]
        },
        {
          "entity": "friendship",
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

# Open a friends-only submission without being a friend

## Trigger

A member who is not the owner's friend opens a friends-only submission.

## Outcome

The submission is not shown.

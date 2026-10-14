---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses to remove all submission notifications",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "notification",
          "effect": "reads",
          "facts": [
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
          "place": "web::community::submission-notifications"
        }
      }
    },
    {
      "text": "The Product removes the submission notifications received up to that point",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "notification",
          "effect": "removes"
        },
        {
          "entity": "submission",
          "effect": "reads",
          "facts": []
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

# Remove all submission notifications up to a point

## Trigger

A member has seen every new submission listed.

## Outcome

Submission notifications up to that point are gone.

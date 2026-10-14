---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects notifications and removes them",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "notification",
          "effect": "reads",
          "facts": [
            "Kind",
            "Subject"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::notifications"
        }
      }
    },
    {
      "text": "The Product removes the selected notifications",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "notification",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::notifications"
        }
      }
    }
  ]
}
---

# Remove selected notifications

## Trigger

A member has dealt with some notifications.

## Outcome

The removed notifications are gone.

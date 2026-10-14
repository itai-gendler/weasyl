---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens their notifications",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "notification",
          "effect": "reads",
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
          "place": "web::community::notifications"
        }
      }
    }
  ]
}
---

# Review notifications

## Trigger

A member sees they have new notifications.

## Outcome

The member sees each notification with who caused it and what it is about.

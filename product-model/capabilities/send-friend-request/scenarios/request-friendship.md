---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Friend on a profile",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Username"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::profile"
        }
      }
    },
    {
      "text": "The Product creates the friend request as a friendship and notifies the other member",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "friendship",
          "effect": "creates",
          "to": "Requested",
          "facts": [
            "Requested at"
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
          "place": "web::community::profile"
        }
      }
    }
  ]
}
---

# Send a friend request

## Trigger

A verified member wants to see someone's friends-only work.

## Outcome

The request waits for the other member, who is notified.

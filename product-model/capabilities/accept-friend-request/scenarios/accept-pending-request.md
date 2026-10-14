---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Accept on a pending friend request",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "friendship",
          "effect": "reads",
          "facts": [
            "Requested at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::friends"
        }
      }
    },
    {
      "text": "The Product accepts the friendship, replaces the request notification and notifies the requester",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "friendship",
          "effect": "changes",
          "from": "Requested",
          "to": "Accepted",
          "facts": [
            "Accepted at"
          ]
        },
        {
          "entity": "notification",
          "as": "request-notice",
          "effect": "removes"
        },
        {
          "entity": "notification",
          "as": "acceptance-notice",
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
          "place": "web::community::friends"
        }
      }
    }
  ]
}
---

# Accept a friend request

## Trigger

A member receives a friend request from someone they know.

## Outcome

They are friends and see each other's friends-only work.

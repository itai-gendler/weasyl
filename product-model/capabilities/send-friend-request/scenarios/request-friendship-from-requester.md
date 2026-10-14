---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Friend on the profile of someone who sent them a friend request",
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
      "text": "The Product accepts the pending friendship and notifies the requester",
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

# Send a friend request to someone who already asked

## Trigger

A member asks for friendship with someone whose request is pending.

## Outcome

The two members are friends and the requester is notified.

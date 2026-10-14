---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Friend Request Sent on a profile",
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
      "text": "The Product removes the friend request and its notification",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "friendship",
          "effect": "removes",
          "from": "Requested"
        },
        {
          "entity": "notification",
          "effect": "removes"
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

# Withdraw a friend request

## Trigger

A member changes their mind about a request.

## Outcome

The request and its notification are gone.

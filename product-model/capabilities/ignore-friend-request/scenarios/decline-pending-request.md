---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Ignore on a pending friend request",
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
          "place": "web::community::friends"
        }
      }
    }
  ]
}
---

# Ignore a friend request

## Trigger

A member does not want to be friends with a requester.

## Outcome

The request is gone.

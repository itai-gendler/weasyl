---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses to unfriend a friend",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "friendship",
          "effect": "reads",
          "facts": [
            "Accepted at"
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
      "text": "The Product removes the friendship and its notification",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "friendship",
          "effect": "removes",
          "from": "Accepted"
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

# Unfriend a member

## Trigger

A member no longer wants to share friends-only work with someone.

## Outcome

They are no longer friends.

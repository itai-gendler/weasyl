---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member removes a member from their ignore list",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "ignore-list-entry",
          "effect": "reads",
          "facts": [
            "Ignored account"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::ignored-users"
        }
      }
    },
    {
      "text": "The Product removes the ignore list entry",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "ignore-list-entry",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::ignored-users"
        }
      }
    }
  ]
}
---

# Unignore a member

## Trigger

A member is ready to see someone again.

## Outcome

The other member's activity shows again.

## Edge cases

- Friendships and follows ended by ignoring do not return.

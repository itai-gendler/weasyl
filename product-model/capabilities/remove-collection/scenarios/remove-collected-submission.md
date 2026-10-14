---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects accepted collections and removes them",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Collected at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::collections"
        }
      }
    },
    {
      "text": "The Product removes the collection and the notifications it sent",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "collection",
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
          "place": "web::community::collections"
        }
      }
    }
  ]
}
---

# Remove a collection

## Trigger

A member no longer wants a collected piece shown.

## Outcome

The submission leaves the member's collections.

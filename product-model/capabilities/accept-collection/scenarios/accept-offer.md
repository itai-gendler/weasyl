---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects offers and chooses Accept",
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
      "text": "The Product accepts the collection and clears its offer notification",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "collection",
          "effect": "changes",
          "from": "Offered",
          "to": "Accepted",
          "facts": [
            "Collected at"
          ]
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

# Accept a collection offer

## Trigger

A member has a collection offer.

## Outcome

The submission shows in the member's collections.

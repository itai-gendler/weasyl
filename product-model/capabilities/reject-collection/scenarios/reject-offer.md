---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects offers and chooses Reject",
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
      "text": "The Product removes the collection offer and its notification",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "collection",
          "effect": "removes",
          "from": "Offered"
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

# Reject a collection offer

## Trigger

A member does not want an offered submission.

## Outcome

The offer is gone.

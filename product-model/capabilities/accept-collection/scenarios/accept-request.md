---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects requests for their submissions and chooses Accept",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "collection",
          "effect": "reads",
          "facts": [
            "Collected at"
          ]
        },
        {
          "entity": "submission",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::collections"
        }
      }
    },
    {
      "text": "The Product accepts the collection and clears its request notification",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "collection",
          "effect": "changes",
          "from": "Requested",
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

# Accept a collection request

## Trigger

An artist has a request for one of their submissions.

## Outcome

The submission shows in the requester's collections.

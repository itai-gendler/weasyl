---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses their settings for requests and alerts and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Collection requests allowed",
            "Collection notifications"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::collection-settings"
        }
      }
    },
    {
      "text": "The Product saves the collection settings on the account",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Collection requests allowed",
            "Collection notifications"
          ]
        },
        {
          "entity": "collection",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::collection-settings"
        }
      }
    }
  ]
}
---

# Save collection settings

## Trigger

A member wants fewer collection requests or notifications.

## Outcome

The settings apply to new requests and activity.

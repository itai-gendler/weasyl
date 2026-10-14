---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Director edits the global restricted tag patterns and saves",
      "kind": "actor",
      "actor": "director",
      "entities": [
        {
          "entity": "global-tagging-restrictions",
          "effect": "reads",
          "facts": [
            "Restricted tags"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::global-tagging-restrictions"
        }
      }
    },
    {
      "text": "The Product saves the global tagging restrictions",
      "kind": "product",
      "actor": "director",
      "entities": [
        {
          "entity": "global-tagging-restrictions",
          "effect": "changes",
          "facts": [
            "Restricted tags"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::global-tagging-restrictions"
        }
      }
    }
  ]
}
---

# Save global tagging restrictions

## Trigger

A director wants a tag kept out of suggestions site-wide.

## Outcome

Matching tags can no longer be suggested anywhere.

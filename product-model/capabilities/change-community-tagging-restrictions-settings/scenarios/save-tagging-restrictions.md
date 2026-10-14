---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member edits their restricted tag patterns and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Community tagging restrictions"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::tagging-restrictions"
        }
      }
    },
    {
      "text": "The Product saves the community tagging restrictions on the account",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Community tagging restrictions"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::tagging-restrictions"
        }
      }
    }
  ]
}
---

# Save community tagging restrictions

## Trigger

A member keeps receiving unwanted tag suggestions.

## Outcome

Matching tags can no longer be suggested on the member's posts.

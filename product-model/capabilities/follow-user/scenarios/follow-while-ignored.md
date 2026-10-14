---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member asks for updates from the member whose profile they are on",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::profile"
        }
      }
    },
    {
      "text": "Either member ignores the other",
      "kind": "condition",
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
          "place": "web::community::profile"
        }
      }
    }
  ]
}
---

# Follow a member who ignores you

## Trigger

A member tries to follow someone who ignores them.

## Outcome

No follow is created.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects notes in their inbox and removes them",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "note",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::notes"
        }
      }
    },
    {
      "text": "The Product marks the notes removed by the recipient",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "note",
          "effect": "changes",
          "facts": [
            "Removed by recipient"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::notes"
        }
      }
    }
  ]
}
---

# Remove notes from the inbox

## Trigger

A member tidies their inbox.

## Outcome

The notes are gone from the member's inbox only.

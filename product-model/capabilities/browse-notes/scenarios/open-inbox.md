---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens their inbox",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "note",
          "effect": "reads",
          "facts": [
            "Title",
            "Sent at"
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

# Open the inbox

## Trigger

A member wants to see their notes.

## Outcome

The member sees their notes, unread ones marked.

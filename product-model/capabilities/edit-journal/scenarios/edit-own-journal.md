---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member changes their journal and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "journal",
          "effect": "reads",
          "facts": [
            "Title",
            "Content",
            "Rating",
            "Friends only"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::journal-details-form"
        }
      }
    },
    {
      "text": "The Product saves the journal",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "journal",
          "effect": "changes",
          "facts": [
            "Title",
            "Content",
            "Rating",
            "Friends only"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::journal-details-form"
        }
      }
    }
  ]
}
---

# Edit a journal

## Trigger

An owner updates a journal entry.

## Outcome

The journal shows the new text.

## Edge cases

- Making a journal friends only removes every notification about it, friends' included.

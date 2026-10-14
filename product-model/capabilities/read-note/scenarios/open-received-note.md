---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens an unread note",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "note",
          "effect": "reads",
          "facts": [
            "Title",
            "Content",
            "Sent at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::note"
        }
      }
    },
    {
      "text": "The Product marks the note read",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "note",
          "effect": "changes",
          "from": "Unread",
          "to": "Read",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::note"
        }
      }
    }
  ]
}
---

# Read a received note

## Trigger

A member has an unread note.

## Outcome

The member reads the note and it is no longer unread.

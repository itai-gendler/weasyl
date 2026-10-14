---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a recipient, a title and a message",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::note-composer"
        }
      }
    },
    {
      "text": "The Product delivers the note unread to the recipient",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "note",
          "effect": "creates",
          "to": "Unread",
          "facts": [
            "Title",
            "Content",
            "Sent at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::note-composer"
        }
      }
    }
  ]
}
---

# Send a note

## Trigger

A verified member wants to message someone privately.

## Outcome

The note is in the recipient's inbox, unread.

## Edge cases

- Sending a note lets its recipient send notes back even if the sender's Notes setting would otherwise refuse them.
- Staff may attach a copy of the note to the recipient's staff notes.

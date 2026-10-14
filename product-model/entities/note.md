---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/note.py#send"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/note.py#select_view"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/note.py#remove_list"
    }
  ]
}
---

# Note

A private message between two members.

## Information kept

- **Title** — the note's subject
- **Content** — the message
- **Sent at** — when it was sent
- **Removed by sender** — whether the sender removed it from their sent messages
- **Removed by recipient** — whether the recipient removed it from their inbox

## States

### Unread

Not yet opened by the recipient.

### Read

Opened by the recipient.

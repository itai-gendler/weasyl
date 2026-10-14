---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "note",
      "effect": "changes",
      "to": "Read"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "receives",
          "entity": "account"
        },
        {
          "verb": "holds",
          "entity": "member"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/note.py#select_view"
    }
  ]
}
---

# Only the recipient's opening marks a note read

Opening a sent note does not change it.

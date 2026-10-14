---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "note",
      "effect": "changes",
      "facts": [
        "Removed by recipient"
      ]
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
      "target": "weasyl/note.py#remove_list"
    }
  ]
}
---

# Only the recipient removes a note from their inbox

The sender keeps their copy.

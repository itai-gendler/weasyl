---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "note",
      "effect": "changes",
      "facts": [
        "Removed by sender"
      ]
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "sends",
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

# Only the sender removes a note from their sent messages

The recipient keeps their copy.

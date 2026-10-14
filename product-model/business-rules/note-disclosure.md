---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "note",
      "effect": "reads"
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
    },
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

# Only the sender and recipient read a note

Staff do not read members' notes unless they are a party to them.

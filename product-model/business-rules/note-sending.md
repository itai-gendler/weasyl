---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "note",
      "effect": "creates"
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
      ],
      "when": [
        {
          "entity": "account",
          "fact": "Verification",
          "is": "Verified"
        }
      ]
    },
    {
      "actors": [
        "moderator",
        "administrator",
        "director"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/note.py#send"
    }
  ]
}
---

# Only verified members send notes, as the recipient allows

The recipient must be verified and not ignore the sender; a recipient taking notes only from friends or staff still takes them from anyone they have sent a note to. Staff closing a report send notes too.

---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "notification",
      "effect": "reads"
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
      "target": "weasyl/message.py#select_notifications"
    }
  ]
}
---

# Members see only their own notifications

Notifications go when their subject is removed, hidden or made friends only, and members clear them themselves.

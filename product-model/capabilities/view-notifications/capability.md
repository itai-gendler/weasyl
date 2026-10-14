---
{
  "availability": [
    {
      "place": "web::community"
    }
  ],
  "domain": "notifications",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/messages.py#messages_notifications_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/message.py#select_notifications"
    }
  ]
}
---

# View notifications

A member reviews their comment, reply, shout, favorite, follow, friend, collection and journal notifications, grouped by kind.

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
      "target": "weasyl/controllers/messages.py#messages_remove_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/message.py#remove_all_before"
    }
  ]
}
---

# Remove notifications

A member clears selected notifications, or all of them up to a point.

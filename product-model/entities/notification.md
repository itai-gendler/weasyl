---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/welcome.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/message.py#select_notifications"
    }
  ]
}
---

# Notification

A message in a member's notifications about activity that concerns them.

## Information kept

- **Kind** — what happened: a new post from someone followed, a comment, reply, favorite, follow, friend request, collection offer or request
- **Sender** — the member whose action caused it
- **Subject** — the post, comment or person it is about
- **Received at** — when it arrived

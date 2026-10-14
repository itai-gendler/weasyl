---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/frienduser.py#request"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/frienduser.py#remove"
    }
  ]
}
---

# Friendship

A friend request between two members and, once accepted, their friendship, which opens friends-only work to each other.

## Information kept

- **Requested at** — when the request was sent
- **Accepted at** — when it was accepted

## States

### Requested

Sent and waiting for the other member.

### Accepted

Both members are friends.

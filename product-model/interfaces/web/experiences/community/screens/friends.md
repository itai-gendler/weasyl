---
{
  "entities": [
    {
      "entity": "friendship",
      "shows": [
        "Requested at",
        "Accepted at"
      ]
    },
    {
      "entity": "account",
      "shows": [
        "Username",
        "Avatar"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/manage/friends_accepted.html"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/manage/friends_pending.html"
    }
  ]
}
---

# Friends

A member's friends and pending friend requests.

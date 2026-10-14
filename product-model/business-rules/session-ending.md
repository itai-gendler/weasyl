---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "session",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "owns",
          "entity": "account"
        },
        {
          "verb": "holds",
          "entity": "member"
        }
      ]
    },
    {
      "actors": [
        "visitor"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/user.py#signout_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/profile.py#invalidate_other_sessions"
    }
  ]
}
---

# A session ends when its member signs out or the account password changes

Changing or resetting the password ends every other session of the account.

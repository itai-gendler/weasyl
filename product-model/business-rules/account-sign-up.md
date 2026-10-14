---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "creates"
    }
  ],
  "permits": [
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
      "target": "weasyl/controllers/user.py#signup_post_"
    }
  ]
}
---

# Visitors sign up for accounts

Anyone not signed in may sign up; a signed-in member cannot reach sign-up.

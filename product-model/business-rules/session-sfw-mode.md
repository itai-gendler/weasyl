---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "session",
      "effect": "changes",
      "facts": [
        "SFW mode"
      ]
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
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/settings.py#sfw_toggle_"
    }
  ]
}
---

# Only the member signed in to a session switches its SFW mode

SFW mode belongs to one browser's session.

---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "staff-note",
      "effect": "creates"
    }
  ],
  "permits": [
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
      "target": "weasyl/controllers/content.py#submit_shout_"
    }
  ]
}
---

# Only staff write staff notes

Moderators, administrators and directors write them; others never see them.

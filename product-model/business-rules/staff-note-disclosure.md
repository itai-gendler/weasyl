---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "staff-note",
      "effect": "reads"
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
      "target": "weasyl/controllers/profile.py#staffnotes_"
    }
  ]
}
---

# Only staff read staff notes

The account they are about never sees them.

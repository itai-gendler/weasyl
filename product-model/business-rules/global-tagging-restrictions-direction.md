---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "global-tagging-restrictions",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "actors": [
        "director"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/director.py#directorcontrol_globaltagrestrictions_post_"
    }
  ]
}
---

# Only directors change the global tagging restrictions

Administrators and moderators who are not directors cannot change them.

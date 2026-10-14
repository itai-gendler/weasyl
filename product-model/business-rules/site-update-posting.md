---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "site-update",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "actors": [
        "administrator",
        "director"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/siteupdate.py#site_update_post_"
    }
  ]
}
---

# Only administrators post site updates

Moderators who are not administrators cannot post them.

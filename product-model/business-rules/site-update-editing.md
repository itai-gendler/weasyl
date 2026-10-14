---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "site-update",
      "effect": "changes"
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
      "target": "weasyl/controllers/siteupdate.py#site_update_put_"
    }
  ]
}
---

# Only administrators edit site updates

Moderators who are not administrators cannot edit them.

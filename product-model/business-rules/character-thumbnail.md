---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "character",
      "effect": "changes",
      "facts": [
        "Thumbnail"
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
    },
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
      "target": "weasyl/controllers/settings.py#manage_thumbnail_post_"
    }
  ]
}
---

# Only the owner or an administrator selects a character's thumbnail

Moderators who are not administrators cannot select it.

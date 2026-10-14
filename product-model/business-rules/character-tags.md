---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "character",
      "effect": "changes",
      "facts": [
        "Tags"
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
      "target": "weasyl/searchtag.py#associate"
    }
  ]
}
---

# Only the owner or staff set the tags of characters

Everyone else may only suggest tags.

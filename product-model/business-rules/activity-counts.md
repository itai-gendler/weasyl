---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "submission",
      "effect": "changes",
      "facts": [
        "Views",
        "Favorites"
      ]
    },
    {
      "type": "entity",
      "id": "character",
      "effect": "changes",
      "facts": [
        "Views"
      ]
    },
    {
      "type": "entity",
      "id": "journal",
      "effect": "changes",
      "facts": [
        "Views"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "visitor",
        "member"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/define.py#common_view_content"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/favorite.py#insert"
    }
  ]
}
---

# Views and favorites are counted as people act

A view counts once per viewer within a short window and never for the owner; favoriting and unfavoriting change the favorites count.

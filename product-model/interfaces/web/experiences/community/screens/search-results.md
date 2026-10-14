---
{
  "entities": [
    {
      "entity": "submission",
      "shows": [
        "Title",
        "Rating",
        "Thumbnail"
      ]
    },
    {
      "entity": "character",
      "shows": [
        "Name",
        "Rating",
        "Thumbnail"
      ]
    },
    {
      "entity": "journal",
      "shows": [
        "Title",
        "Rating"
      ]
    },
    {
      "entity": "account",
      "shows": [
        "Username",
        "Avatar"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/search.py#select"
    },
    {
      "kind": "doc",
      "role": "context",
      "target": "weasyl/templates/help/searching.html"
    }
  ]
}
---

# Search

Posts found by tags, or people found by name.

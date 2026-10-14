---
{
  "entities": [
    {
      "entity": "character",
      "shows": [
        "Name",
        "Age",
        "Gender",
        "Height",
        "Weight",
        "Species",
        "Description",
        "Rating",
        "Tags",
        "Friends only",
        "Image",
        "Posted at",
        "Views"
      ]
    },
    {
      "entity": "comment",
      "shows": [
        "Content",
        "Posted at",
        "Reply to"
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
      "target": "weasyl/templates/detail/character.html"
    }
  ]
}
---

# Character page

One character with its details, tags and comments.

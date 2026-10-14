---
{
  "entities": [
    {
      "entity": "journal",
      "shows": [
        "Title",
        "Content",
        "Rating",
        "Tags",
        "Friends only",
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
      "target": "weasyl/templates/detail/journal.html"
    }
  ]
}
---

# Journal page

One journal entry with its tags and comments.

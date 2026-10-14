---
{
  "entities": [
    {
      "entity": "submission",
      "shows": [
        "Title",
        "Description",
        "Category",
        "Rating",
        "Tags",
        "Friends only",
        "Critique requested",
        "Submission file",
        "Cover art",
        "Embedded media",
        "Posted at",
        "Views",
        "Favorites",
        "Folder"
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
      "target": "weasyl/templates/detail/submission.html"
    }
  ]
}
---

# Submission page

One submission with its artist, details, tags and comments.

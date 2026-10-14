---
{
  "entities": [
    {
      "entity": "submission",
      "shows": [
        "Title",
        "Rating",
        "Friends only",
        "Critique requested",
        "Thumbnail"
      ]
    },
    {
      "entity": "character",
      "shows": [
        "Name",
        "Rating",
        "Friends only"
      ]
    },
    {
      "entity": "journal",
      "shows": [
        "Title",
        "Rating",
        "Friends only"
      ]
    },
    {
      "entity": "account",
      "shows": [
        "Username"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/modcontrol/contentbyuser.html"
    }
  ]
}
---

# Content by user

Every submission, character and journal of one account, hidden ones included, for moderation in bulk.

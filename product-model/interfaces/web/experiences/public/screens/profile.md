---
{
  "entities": [
    {
      "entity": "account",
      "shows": [
        "Username",
        "Full name",
        "Catchphrase",
        "Profile text",
        "Avatar",
        "Profile details",
        "Joined at"
      ]
    },
    {
      "entity": "submission",
      "shows": [
        "Title",
        "Rating",
        "Thumbnail"
      ]
    },
    {
      "entity": "folder",
      "shows": [
        "Title"
      ]
    },
    {
      "entity": "character",
      "shows": [
        "Name",
        "Thumbnail"
      ]
    },
    {
      "entity": "journal",
      "shows": [
        "Title",
        "Posted at"
      ]
    },
    {
      "entity": "favorite",
      "shows": [
        "Favorited at"
      ]
    },
    {
      "entity": "shout",
      "shows": [
        "Content",
        "Posted at",
        "Reply to"
      ]
    },
    {
      "entity": "collection",
      "shows": [
        "Collected at"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/profile.py#profile_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/user/profile.html"
    }
  ]
}
---

# Profile

A member's profile with its tabs: gallery and folders, characters, journals, favorites, collections, shouts, friends and followers.

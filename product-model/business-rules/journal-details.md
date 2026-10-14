---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "journal",
      "effect": "changes",
      "facts": [
        "Title",
        "Content",
        "Rating",
        "Friends only"
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
      "target": "weasyl/journal.py#edit"
    }
  ]
}
---

# Only the owner or staff change the details of journals

Edits by staff are recorded in the owner's staff notes, and staff may set any rating; an owner may use only the ratings their age allows.

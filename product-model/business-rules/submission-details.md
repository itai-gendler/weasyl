---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "submission",
      "effect": "changes",
      "facts": [
        "Title",
        "Description",
        "Category",
        "Rating",
        "Folder",
        "Friends only",
        "Critique requested"
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
      "target": "weasyl/submission.py#edit"
    }
  ]
}
---

# Only the owner or staff change the details of submissions

Edits by staff are recorded in the owner's staff notes, and staff may set any rating; an owner may use only the ratings their age allows.

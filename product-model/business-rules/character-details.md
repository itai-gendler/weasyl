---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "character",
      "effect": "changes",
      "facts": [
        "Name",
        "Age",
        "Gender",
        "Height",
        "Weight",
        "Species",
        "Description",
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
      "target": "weasyl/character.py#edit"
    }
  ]
}
---

# Only the owner or staff change the details of characters

Edits by staff are recorded in the owner's staff notes, and staff may set any rating; an owner may use only the ratings their age allows.

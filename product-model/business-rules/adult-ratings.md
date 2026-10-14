---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "submission",
      "effect": "creates",
      "facts": [
        "Rating"
      ]
    },
    {
      "type": "entity",
      "id": "character",
      "effect": "creates",
      "facts": [
        "Rating"
      ]
    },
    {
      "type": "entity",
      "id": "journal",
      "effect": "creates",
      "facts": [
        "Rating"
      ]
    },
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Maximum viewable rating"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/profile.py#check_user_rating_allowed"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/profile.py#assert_adult"
    }
  ]
}
---

# Mature and Explicit work needs an adult

Posting or choosing to see Mature or Explicit work records that the person confirmed being 18 or older, and someone whose recorded birthday makes them younger may not use those ratings.

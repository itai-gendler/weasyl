---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator selects characters among the content of an account and chooses a rating",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "character",
          "effect": "reads",
          "facts": [
            "Name",
            "Rating"
          ]
        },
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::user-content"
        }
      }
    },
    {
      "text": "The Product changes the rating of each character and adds a staff note listing the changes",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "character",
          "effect": "changes",
          "facts": [
            "Rating"
          ]
        },
        {
          "entity": "staff-note",
          "effect": "creates",
          "facts": [
            "Content",
            "Written at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::user-content"
        }
      }
    }
  ]
}
---

# Re-rate several characters of an account

## Trigger

A moderator reviews an account's characters.

## Outcome

The characters have the new rating.

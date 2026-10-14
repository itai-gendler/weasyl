---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member changes the details of their character and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
          "effect": "reads",
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
      "contexts": {
        "web": {
          "place": "web::community::character-details-form"
        }
      }
    },
    {
      "text": "The Product saves the details of the character",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
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
      "contexts": {
        "web": {
          "place": "web::community::character-details-form"
        }
      }
    }
  ]
}
---

# Edit a character

## Trigger

An owner updates their character.

## Outcome

The character shows the new details.

## Edge cases

- Making a character friends only removes every notification about it.

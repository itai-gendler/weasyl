---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the character",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
          "effect": "reads",
          "facts": [
            "Name",
            "Species",
            "Description",
            "Rating",
            "Tags",
            "Image",
            "Posted at",
            "Views"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::character-page"
        }
      }
    },
    {
      "text": "The Product counts the view unless the member owns the character",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
          "effect": "changes",
          "facts": [
            "Views"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::character-page"
        }
      }
    }
  ]
}
---

# View a character as a member

## Trigger

A member opens a character.

## Outcome

The member sees the character with its actions.

## Edge cases

- A character rated above the member's maximum viewable rating is refused rather than offered behind a warning.

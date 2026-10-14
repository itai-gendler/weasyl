---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the character",
      "kind": "actor",
      "actor": "visitor",
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
          "place": "web::public::character-page"
        }
      }
    },
    {
      "text": "The Product counts the view",
      "kind": "product",
      "actor": "visitor",
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
          "place": "web::public::character-page"
        }
      }
    }
  ]
}
---

# View a character as a visitor

## Trigger

A visitor opens a General character.

## Outcome

The visitor sees the character and its comments.

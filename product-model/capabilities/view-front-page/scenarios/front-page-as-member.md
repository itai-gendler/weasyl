---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the front page",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Thumbnail"
          ]
        },
        {
          "entity": "journal",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::front-page"
        }
      }
    }
  ]
}
---

# See the front page as a member

## Trigger

A member opens the front page.

## Outcome

The member sees recent work within their rating, without people they ignore or tags they block.

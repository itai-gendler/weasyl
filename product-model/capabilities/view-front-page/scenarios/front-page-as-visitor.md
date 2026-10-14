---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the front page",
      "kind": "actor",
      "actor": "visitor",
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
          "place": "web::public::front-page"
        }
      }
    }
  ]
}
---

# See the front page as a visitor

## Trigger

A visitor arrives at Weasyl.

## Outcome

The visitor sees recent General work.

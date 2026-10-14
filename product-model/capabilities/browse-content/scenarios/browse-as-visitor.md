---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the latest artwork",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Rating",
            "Thumbnail"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::browse"
        }
      }
    }
  ]
}
---

# Browse the latest artwork as a visitor

## Trigger

A visitor wants to see new work.

## Outcome

The visitor pages through recent General artwork.

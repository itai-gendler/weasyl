---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor enters tags to search for",
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
          "place": "web::public::search-results"
        }
      }
    }
  ]
}
---

# Search by tags as a visitor

## Trigger

A visitor looks for work on a subject.

## Outcome

The visitor sees matching General posts.

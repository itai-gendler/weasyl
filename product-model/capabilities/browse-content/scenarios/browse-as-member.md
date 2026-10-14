---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the latest artwork in a category",
      "kind": "actor",
      "actor": "member",
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
          "place": "web::community::browse"
        }
      }
    }
  ]
}
---

# Browse the latest artwork as a member

## Trigger

A member wants to see new work.

## Outcome

The member pages through recent work within their rating and filters.

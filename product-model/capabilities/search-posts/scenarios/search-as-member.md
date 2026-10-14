---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters tags and limits the search to posts they starred",
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
          "place": "web::community::search-results"
        }
      }
    }
  ]
}
---

# Search within favorites as a member

## Trigger

A member looks for something they favorited.

## Outcome

The member sees matching posts among their favorites, within their rating and filters.

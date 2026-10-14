---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Favorited on a submission they favorited",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Favorites"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-page"
        }
      }
    },
    {
      "text": "The Product removes the favorite, uncounts it on the submission and removes its notifications",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "favorite",
          "effect": "removes"
        },
        {
          "entity": "submission",
          "effect": "changes",
          "facts": [
            "Favorites"
          ]
        },
        {
          "entity": "notification",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-page"
        }
      }
    }
  ]
}
---

# Unfavorite a submission

## Trigger

A member changes their mind about a favorite.

## Outcome

The submission leaves the member's favorites.

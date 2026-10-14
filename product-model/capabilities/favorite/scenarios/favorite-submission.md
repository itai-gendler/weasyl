---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member stars a submission",
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
      "text": "The Product records the favorite, counts it on the submission and notifies its owner and collectors",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "favorite",
          "effect": "creates",
          "facts": [
            "Favorited at"
          ]
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
          "effect": "creates",
          "facts": [
            "Kind",
            "Sender",
            "Subject",
            "Received at"
          ]
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

# Favorite a submission

## Trigger

A member likes a submission.

## Outcome

The submission is in the member's favorites and its favorites count grows.

## Edge cases

- Characters and journals are favorited the same way but keep no favorites count.
- Favoriting is refused when either member ignores the other, or when the post is friends only and the member is not a friend.

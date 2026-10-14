---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the submission",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Description",
            "Category",
            "Rating",
            "Tags",
            "Submission file",
            "Cover art",
            "Posted at",
            "Views",
            "Favorites"
          ]
        },
        {
          "entity": "comment",
          "effect": "reads",
          "facts": [
            "Content",
            "Posted at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::submission-page"
        }
      }
    },
    {
      "text": "The Product counts the view",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "submission",
          "effect": "changes",
          "facts": [
            "Views"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::submission-page"
        }
      }
    }
  ]
}
---

# View a General submission as a visitor

## Trigger

A visitor follows a link to a submission.

## Outcome

The visitor sees the submission, its tags, favorites count and comments.

## Edge cases

- Friends-only submissions are never shown to visitors.

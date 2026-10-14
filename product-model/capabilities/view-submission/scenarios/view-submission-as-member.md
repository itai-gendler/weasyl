---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the submission",
      "kind": "actor",
      "actor": "member",
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
          "place": "web::community::submission-page"
        }
      }
    },
    {
      "text": "The Product counts the view unless the member owns the submission",
      "kind": "product",
      "actor": "member",
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
          "place": "web::community::submission-page"
        }
      }
    }
  ]
}
---

# View a submission as a member

## Trigger

A member opens a submission.

## Outcome

The member sees the submission with favorite, tag, comment, report and collection actions.

## Edge cases

- A submission by someone the member ignores, or with a tag they block, is withheld until the member chooses to view it anyway.
- A member of unknown age who views a Mature or Explicit submission past the warning is recorded as confirming they are 18 or older.

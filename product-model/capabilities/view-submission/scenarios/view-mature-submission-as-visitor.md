---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens a Mature submission",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::submission-page"
        }
      }
    },
    {
      "text": "The rating is above what the visitor may see",
      "kind": "condition",
      "actor": "visitor",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Rating"
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
      "text": "The Visitor confirms being 18 or older and chooses to view this submission",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Rating",
            "Submission file"
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

# Open a submission above General as a visitor

## Trigger

A visitor opens a Mature or Explicit submission.

## Outcome

The visitor is asked to confirm they are 18 or older and may then view this one submission.

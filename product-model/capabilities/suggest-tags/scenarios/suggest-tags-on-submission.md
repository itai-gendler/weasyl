---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member adds tags to the tag list of another member's submission and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Tags"
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
      "text": "The Product records each new tag as a tag suggestion by the member",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "tag-suggestion",
          "effect": "creates",
          "to": "Suggested",
          "facts": [
            "Tag",
            "Suggested by"
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

# Suggest tags on a submission

## Trigger

A member sees a submission missing useful tags.

## Outcome

The new tags are suggestions on the submission.

## Edge cases

- Saving again replaces the member's own earlier suggestions that are still pending.
- A member the owner ignores cannot suggest tags on the owner's posts.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator edits the tag list of a member's submission and saves",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Tags"
          ]
        },
        {
          "entity": "member",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-page"
        }
      }
    },
    {
      "text": "The Product replaces the tags of the submission and records the change in its tag history",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "submission",
          "effect": "changes",
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
    }
  ]
}
---

# Correct tags as staff

## Trigger

A moderator fixes the tags of a member's submission.

## Outcome

The submission has the corrected tags.

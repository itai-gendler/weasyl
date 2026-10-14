---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member flags a submission for staff, picks a violation and writes an explanation",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title"
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
      "text": "The Product opens a report on the submission with the member's violation and explanation",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "report",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Reported item",
            "Violation",
            "Report comments",
            "Opened at"
          ]
        },
        {
          "entity": "submission",
          "effect": "reads",
          "facts": []
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

# Report a submission

## Trigger

A member finds a submission that breaks the rules.

## Outcome

Staff have an open report on the submission.

## Edge cases

- Violations such as tracing or plagiarism need a comment.

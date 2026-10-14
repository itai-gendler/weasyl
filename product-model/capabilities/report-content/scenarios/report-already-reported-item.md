---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member flags a journal for staff, picks a violation and writes an explanation",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "journal",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::journal-page"
        }
      }
    },
    {
      "text": "Someone already flagged the journal and staff have not closed it yet",
      "kind": "condition",
      "entities": [
        {
          "entity": "journal",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::journal-page"
        }
      }
    },
    {
      "text": "The Product adds the member's violation and explanation to the open report",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "report",
          "effect": "changes",
          "facts": [
            "Violation",
            "Report comments"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::journal-page"
        }
      }
    }
  ]
}
---

# Report an item that already has an open report

## Trigger

A member reports a journal someone else reported.

## Outcome

The member's comment joins the existing open report.

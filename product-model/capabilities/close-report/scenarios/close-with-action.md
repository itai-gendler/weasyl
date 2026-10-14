---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator chooses Close: action taken and writes an explanation and a message to the owner",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "report",
          "effect": "reads",
          "facts": [
            "Reported item",
            "Violation",
            "Report comments",
            "Assigned moderator",
            "Opened at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::report"
        }
      }
    },
    {
      "text": "The Product closes the report, sends the note to the owner and adds the note to their staff notes",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "report",
          "effect": "changes",
          "from": "Open",
          "to": "Closed",
          "facts": [
            "Assigned moderator",
            "Closure reason",
            "Closure explanation"
          ]
        },
        {
          "entity": "note",
          "effect": "creates",
          "to": "Unread",
          "facts": [
            "Title",
            "Content",
            "Sent at"
          ]
        },
        {
          "entity": "staff-note",
          "effect": "creates",
          "facts": [
            "Content",
            "Written at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::report"
        }
      }
    }
  ]
}
---

# Close a report with action taken

## Trigger

A moderator acted on the reported item.

## Outcome

The report is closed, the owner receives a note from the moderator, and their staff notes keep a copy.

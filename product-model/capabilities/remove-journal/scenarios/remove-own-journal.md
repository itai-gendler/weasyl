---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses to remove their journal and confirms",
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
      "text": "The Product hides the journal and removes the notifications about it",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "journal",
          "effect": "changes",
          "from": "Visible",
          "to": "Hidden",
          "facts": []
        },
        {
          "entity": "notification",
          "effect": "removes"
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

# Remove a journal

## Trigger

An owner no longer wants a journal shown.

## Outcome

The journal is gone from the profile and notifications.

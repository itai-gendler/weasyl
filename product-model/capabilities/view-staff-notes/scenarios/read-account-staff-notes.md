---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator opens the staff notes of an account",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "staff-note",
          "effect": "reads",
          "facts": [
            "Content",
            "Written at"
          ]
        },
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::staff-notes"
        }
      }
    }
  ]
}
---

# Read an account's staff notes

## Trigger

A moderator looks into an account's history.

## Outcome

The moderator sees every staff note, newest first.

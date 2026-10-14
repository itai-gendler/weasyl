---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator writes a staff note on an account",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "staff-note",
          "effect": "reads",
          "facts": []
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
    },
    {
      "text": "The Product adds the staff note",
      "kind": "product",
      "actor": "moderator",
      "entities": [
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
          "place": "web::staff::staff-notes"
        }
      }
    }
  ]
}
---

# Write a staff note

## Trigger

A moderator wants other staff to know something about an account.

## Outcome

The note is among the account's staff notes.

## Edge cases

- A moderator may also copy a note they received into the sender's staff notes.

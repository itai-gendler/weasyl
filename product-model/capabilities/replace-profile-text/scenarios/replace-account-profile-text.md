---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator opens an account in user management and enters replacement profile text",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Username",
            "Profile text"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::user-management"
        }
      }
    },
    {
      "text": "The Product replaces the profile text of the account and adds a staff note with the old and new text",
      "kind": "product",
      "actor": "moderator",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Profile text"
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
          "place": "web::staff::user-management"
        }
      }
    }
  ]
}
---

# Replace profile text

## Trigger

A moderator finds rule-breaking profile text.

## Outcome

The profile shows the new text and its staff notes keep the old one.

## Edge cases

- The catchphrase is replaced the same way.

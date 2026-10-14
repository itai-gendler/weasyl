---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member adds a staff member to their ignore list",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::ignored-users"
        }
      }
    },
    {
      "text": "The person is staff, or the member themself",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "ignore-list-entry",
          "effect": "reads",
          "facts": [
            "Ignored account"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::ignored-users"
        }
      }
    }
  ]
}
---

# Ignore a staff member

## Trigger

A member tries to ignore a moderator.

## Outcome

Nobody is ignored.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens a site update",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "site-update",
          "effect": "reads",
          "facts": [
            "Title",
            "Content",
            "Posted at"
          ]
        },
        {
          "entity": "comment",
          "effect": "reads",
          "facts": [
            "Content",
            "Posted at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::site-update"
        }
      }
    }
  ]
}
---

# Read a site update as a member

## Trigger

A member sees there is a new site update.

## Outcome

The member reads it and it no longer shows as new.

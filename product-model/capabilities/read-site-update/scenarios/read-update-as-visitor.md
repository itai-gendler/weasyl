---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens a site update",
      "kind": "actor",
      "actor": "visitor",
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
          "place": "web::public::site-update"
        }
      }
    }
  ]
}
---

# Read a site update as a visitor

## Trigger

A visitor follows a link to staff news.

## Outcome

The visitor reads the update and its comments.

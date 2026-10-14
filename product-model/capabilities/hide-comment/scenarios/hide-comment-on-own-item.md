---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Hide on a comment under their submission",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "comment",
          "effect": "reads",
          "facts": [
            "Content"
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
    },
    {
      "text": "The Product hides the comment and removes its notifications",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "comment",
          "effect": "changes",
          "from": "Visible",
          "to": "Hidden",
          "facts": [
            "Hidden by"
          ]
        },
        {
          "entity": "notification",
          "effect": "removes"
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

# Hide a comment on an own submission

## Trigger

An owner does not want a comment under their work.

## Outcome

The comment and its replies are hidden and their notifications removed.

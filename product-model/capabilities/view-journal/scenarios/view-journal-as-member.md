---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the journal",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "journal",
          "effect": "reads",
          "facts": [
            "Title",
            "Content",
            "Rating",
            "Tags",
            "Posted at",
            "Views"
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
      "text": "The Product counts the view unless the member owns the journal",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "journal",
          "effect": "changes",
          "facts": [
            "Views"
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

# View a journal as a member

## Trigger

A member opens a journal.

## Outcome

The member reads the journal with its actions.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the journal",
      "kind": "actor",
      "actor": "visitor",
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
          "place": "web::public::journal-page"
        }
      }
    },
    {
      "text": "The Product counts the view",
      "kind": "product",
      "actor": "visitor",
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
          "place": "web::public::journal-page"
        }
      }
    }
  ]
}
---

# View a journal as a visitor

## Trigger

A visitor opens a General journal.

## Outcome

The visitor reads the journal and its comments.

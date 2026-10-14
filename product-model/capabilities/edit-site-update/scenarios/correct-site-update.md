---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator changes a site update and saves",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "site-update",
          "effect": "reads",
          "facts": [
            "Title",
            "Content",
            "Posted as mascot"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::site-update-form"
        }
      }
    },
    {
      "text": "The Product saves the site update",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "site-update",
          "effect": "changes",
          "facts": [
            "Title",
            "Content",
            "Posted as mascot"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::site-update-form"
        }
      }
    }
  ]
}
---

# Edit a site update

## Trigger

Staff need to correct news.

## Outcome

The update shows the new text.

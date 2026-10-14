---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator writes a title and content and posts",
      "kind": "actor",
      "actor": "administrator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::site-update-form"
        }
      }
    },
    {
      "text": "The Product creates the site update",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "site-update",
          "effect": "creates",
          "facts": [
            "Title",
            "Content",
            "Posted as mascot",
            "Posted at"
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
      "text": "The site update is shown",
      "kind": "condition",
      "entities": [
        {
          "entity": "site-update",
          "effect": "reads",
          "facts": [
            "Title",
            "Content"
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

# Post a site update

## Trigger

Staff have news for the community.

## Outcome

The update is listed and shows as new to members.

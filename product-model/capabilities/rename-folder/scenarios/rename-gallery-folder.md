---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member picks a folder and enters a new title",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "folder",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-folders"
        }
      }
    },
    {
      "text": "The Product renames the folder",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "folder",
          "effect": "changes",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-folders"
        }
      }
    }
  ]
}
---

# Rename a folder

## Trigger

A member wants a clearer folder name.

## Outcome

The folder shows the new title.

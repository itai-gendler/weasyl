---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a folder title and optionally a parent folder",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "folder",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-folders"
        }
      }
    },
    {
      "text": "The Product creates the folder",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "folder",
          "effect": "creates",
          "facts": [
            "Title",
            "Parent folder"
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

# Create a folder

## Trigger

A member wants to organize their gallery.

## Outcome

The folder is available for submissions.

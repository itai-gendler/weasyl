---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member picks a folder and removes it",
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
      "text": "The Product removes the folder and its subfolders and moves their submissions to the root",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "folder",
          "effect": "removes"
        },
        {
          "entity": "submission",
          "effect": "changes",
          "facts": [
            "Folder"
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

# Remove a folder

## Trigger

A member no longer needs a folder.

## Outcome

The folder is gone and its submissions are in the root.

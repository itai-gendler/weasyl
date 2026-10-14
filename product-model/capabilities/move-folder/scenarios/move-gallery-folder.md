---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member picks a folder and its new parent",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "folder",
          "effect": "reads",
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
    },
    {
      "text": "The Product moves the folder",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "folder",
          "effect": "changes",
          "facts": [
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

# Move a folder

## Trigger

A member reorganizes their folders.

## Outcome

The folder sits under its new parent.

## Edge cases

- A folder that has subfolders, or a parent that is itself a subfolder, is refused: folders nest one level deep.

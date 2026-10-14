---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a folder title already used in the same place",
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
      "text": "A folder with that title already exists under the same parent",
      "kind": "condition",
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
    }
  ]
}
---

# Create a folder with a title already used

## Trigger

A member reuses a sibling folder title.

## Outcome

No folder is created.

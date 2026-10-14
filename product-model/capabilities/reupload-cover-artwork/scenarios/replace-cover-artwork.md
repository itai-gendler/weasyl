---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member uploads new cover artwork for their submission",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::file-reupload"
        }
      }
    },
    {
      "text": "The Product replaces the cover art of the submission",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "changes",
          "facts": [
            "Cover art"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::file-reupload"
        }
      }
    }
  ]
}
---

# Replace cover artwork

## Trigger

An owner wants a new cover for their story or song.

## Outcome

The submission shows the new cover.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses a new file for their submission",
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
      "text": "The Product replaces the file of the submission and regenerates its display copy and generated thumbnail",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "changes",
          "facts": [
            "Submission file",
            "Cover art",
            "Thumbnail"
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

# Replace the submission file

## Trigger

An owner wants to post a corrected version of their work.

## Outcome

The submission shows the new file with regenerated display copy and thumbnail.

## Edge cases

- Visual work accepts JPEG, PNG or GIF and multimedia MP3 or Flash, within the same size limits as submitting.
- A file identical to another of the member's visible submissions is refused.

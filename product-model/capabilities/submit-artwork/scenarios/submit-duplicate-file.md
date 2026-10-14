---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member uploads a file and enters its details",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::artwork-form"
        }
      }
    },
    {
      "text": "The same file is already the file of one of the member's visible submissions",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Submission file"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::artwork-form"
        }
      }
    }
  ]
}
---

# Submit a file already in the gallery

## Trigger

A member uploads a file identical to one of their visible submissions.

## Outcome

Nothing is posted and the member is told it is a duplicate.

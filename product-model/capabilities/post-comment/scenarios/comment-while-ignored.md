---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member writes a comment on a submission",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "comment",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-page"
        }
      }
    },
    {
      "text": "The owner of the submission ignores the member, or the member ignores the owner",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "ignore-list-entry",
          "effect": "reads",
          "facts": [
            "Ignored account"
          ]
        },
        {
          "entity": "submission",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-page"
        }
      }
    }
  ]
}
---

# Comment where the owner ignores the member

## Trigger

A member comments on work by someone who ignores them.

## Outcome

No comment is posted and the member is told the owner ignores them.

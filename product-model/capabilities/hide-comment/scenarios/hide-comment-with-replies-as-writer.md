---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Hide on their own comment",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "comment",
          "effect": "reads",
          "facts": [
            "Content"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-page"
        }
      }
    },
    {
      "text": "The member does not own the submission and the comment has visible replies",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "comment",
          "effect": "reads",
          "facts": [
            "Reply to"
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

# Hide an own comment that has replies

## Trigger

A commenter tries to hide their comment after someone replied.

## Outcome

The comment stays.

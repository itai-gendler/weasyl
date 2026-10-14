---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the submission form",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::artwork-form"
        }
      }
    },
    {
      "text": "The account of the member is unverified",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Verification"
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

# Submit before verification

## Trigger

A member whose account nobody has vouched for opens Submit.

## Outcome

Nothing can be posted and the member is pointed to account verification.

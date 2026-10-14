---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member rejects a suggested tag on their submission",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Tags"
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
      "text": "The Product removes the tag suggestion",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "tag-suggestion",
          "effect": "removes",
          "from": "Suggested"
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

# Reject a suggested tag

## Trigger

An owner disagrees with a suggested tag.

## Outcome

The suggestion is gone.

## Edge cases

- The rejection can be undone for a short while, restoring the suggestion.
- The owner may say why: incorrect, unwanted or abusive.

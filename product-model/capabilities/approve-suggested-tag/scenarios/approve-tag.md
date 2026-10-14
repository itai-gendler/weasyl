---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member approves a suggested tag on their submission",
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
      "text": "The Product approves the tag suggestion and adds it to the tags of the submission",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "tag-suggestion",
          "effect": "changes",
          "from": "Suggested",
          "to": "Approved",
          "facts": []
        },
        {
          "entity": "submission",
          "effect": "changes",
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
    }
  ]
}
---

# Approve a suggested tag

## Trigger

An owner agrees with a suggested tag.

## Outcome

The tag is one of the submission's tags.

## Edge cases

- The approval can be undone for a short while, returning the tag to a suggestion.

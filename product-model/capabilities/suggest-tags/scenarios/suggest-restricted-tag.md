---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member adds tags to another member's submission and saves",
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
          "place": "web::community::submission-page"
        }
      }
    },
    {
      "text": "A tag matches the community tagging restrictions of the owner or the global tagging restrictions",
      "kind": "condition",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Community tagging restrictions"
          ]
        },
        {
          "entity": "global-tagging-restrictions",
          "effect": "reads",
          "facts": [
            "Restricted tags"
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
      "text": "The Product records only the unrestricted tags as tag suggestions",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "tag-suggestion",
          "effect": "creates",
          "to": "Suggested",
          "facts": [
            "Tag",
            "Suggested by"
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

# Suggest a restricted tag

## Trigger

A member suggests a tag the owner or the site restricts.

## Outcome

The other tags are suggested and the member is told which tags were restricted.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member selects blocked tags and removes them",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "tag-filter",
          "effect": "reads",
          "facts": [
            "Tag",
            "Rating threshold"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::blocked-tags"
        }
      }
    },
    {
      "text": "The Product removes the blocked tag",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "tag-filter",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::blocked-tags"
        }
      }
    }
  ]
}
---

# Unblock a tag

## Trigger

A member wants to see a blocked tag again.

## Outcome

Posts with the tag show again.

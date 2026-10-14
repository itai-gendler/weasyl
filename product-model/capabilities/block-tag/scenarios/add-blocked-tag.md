---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a tag and the rating from which to block it",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::blocked-tags"
        }
      }
    },
    {
      "text": "The Product adds the blocked tag for the member",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "tag-filter",
          "effect": "creates",
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
    }
  ]
}
---

# Block a tag

## Trigger

A member does not want to see work with a tag.

## Outcome

Posts with the tag at or above the threshold are hidden from the member.

## Edge cases

- Blocking a tag already blocked changes its rating threshold.

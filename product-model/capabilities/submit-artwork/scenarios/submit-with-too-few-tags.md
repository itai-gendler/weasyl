---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a file, title, rating and a single tag",
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
      "text": "Fewer than two tags were given",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::artwork-form"
        }
      }
    }
  ]
}
---

# Submit with fewer than two tags

## Trigger

A member submits with one tag or none.

## Outcome

Nothing is posted and the member is asked for at least two tags.

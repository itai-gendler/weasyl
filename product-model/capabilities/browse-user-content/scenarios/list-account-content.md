---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Moderator enters a username and the kinds of content to list",
      "kind": "actor",
      "actor": "moderator",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Rating",
            "Friends only"
          ]
        },
        {
          "entity": "character",
          "effect": "reads",
          "facts": [
            "Name",
            "Rating"
          ]
        },
        {
          "entity": "journal",
          "effect": "reads",
          "facts": [
            "Title",
            "Rating"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::user-content"
        }
      }
    }
  ]
}
---

# List an account's content

## Trigger

A moderator investigates an account.

## Outcome

The moderator sees all of its posts newest first.

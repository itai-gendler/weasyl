---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Ignore on a profile",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Username"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::profile"
        }
      }
    },
    {
      "text": "The Product adds the member to the ignore list and removes their friendship and the follow of them",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "ignore-list-entry",
          "effect": "creates",
          "facts": [
            "Ignored account"
          ]
        },
        {
          "entity": "friendship",
          "effect": "removes",
          "from": "Accepted"
        },
        {
          "entity": "follow",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::profile"
        }
      }
    }
  ]
}
---

# Ignore a member

## Trigger

A member wants nothing more to do with someone.

## Outcome

The other member is on the ignore list and no longer a friend or followed.

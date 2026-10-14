---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses to sign out",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community"
        }
      }
    },
    {
      "text": "The Product ends the session",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "session",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community"
        }
      }
    }
  ]
}
---

# Sign out

## Trigger

A member is done using Weasyl.

## Outcome

The session ends and the member lands on the front page as a visitor.

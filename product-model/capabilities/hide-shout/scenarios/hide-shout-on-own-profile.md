---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Hide on a shout on their profile",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "shout",
          "effect": "reads",
          "facts": [
            "Content"
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
      "text": "The Product hides the shout and removes its notifications",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "shout",
          "effect": "changes",
          "from": "Visible",
          "to": "Hidden",
          "facts": [
            "Hidden by"
          ]
        },
        {
          "entity": "notification",
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

# Hide a shout on an own profile

## Trigger

A member does not want a shout on their profile.

## Outcome

The shout is hidden and its notification removed.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Edit Settings beside one member on the list",
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
          "place": "web::community::followed-users"
        }
      }
    },
    {
      "text": "The Member chooses which activity of that member to hear about and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "follow",
          "effect": "reads",
          "facts": [
            "Notification kinds"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::followed-user"
        }
      }
    },
    {
      "text": "The Product saves the notification kinds of the follow",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "follow",
          "effect": "changes",
          "facts": [
            "Notification kinds"
          ]
        },
        {
          "entity": "notification",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::followed-user"
        }
      }
    }
  ]
}
---

# Save follow settings for one member

## Trigger

A member wants fewer notifications from someone.

## Outcome

Only the chosen kinds of activity notify the member.

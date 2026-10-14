---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member writes a shout on a profile",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Username"
          ]
        },
        {
          "entity": "shout",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::profile"
        }
      }
    },
    {
      "text": "The Product posts the shout and notifies the profile owner",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "shout",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Content",
            "Posted at"
          ]
        },
        {
          "entity": "notification",
          "effect": "creates",
          "facts": [
            "Kind",
            "Sender",
            "Subject",
            "Received at"
          ]
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

# Shout on a profile

## Trigger

A verified member wants to leave a message on a profile.

## Outcome

The shout shows on the profile and its owner is notified.

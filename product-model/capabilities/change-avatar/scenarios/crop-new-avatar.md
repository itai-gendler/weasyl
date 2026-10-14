---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member uploads an image and selects the square to use",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Avatar"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::avatar-editor"
        }
      }
    },
    {
      "text": "The Product saves the cropped avatar on the account",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Avatar"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::avatar-editor"
        }
      }
    }
  ]
}
---

# Upload and crop an avatar

## Trigger

A member wants a new profile picture.

## Outcome

The new avatar shows on the profile and beside the member's posts.

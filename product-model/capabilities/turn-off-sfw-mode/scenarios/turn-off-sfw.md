---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses SFW off",
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
      "text": "The Product turns off SFW mode for the session",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "session",
          "effect": "changes",
          "facts": [
            "SFW mode"
          ]
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

# Turn off SFW mode

## Trigger

A member no longer needs SFW mode.

## Outcome

Work up to the member's maximum viewable rating is shown again.

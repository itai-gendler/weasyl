---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses their preferences and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Maximum viewable rating",
            "Custom thumbnails",
            "Hidden from guests",
            "Statistics hidden",
            "Favorites hidden",
            "Shouts from",
            "Notes from",
            "Default follow settings"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::site-preferences"
        }
      }
    },
    {
      "text": "The Product saves the preferences on the account, recording an adult confirmation when Mature or Explicit is chosen",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Maximum viewable rating",
            "Custom thumbnails",
            "Hidden from guests",
            "Statistics hidden",
            "Favorites hidden",
            "Shouts from",
            "Notes from",
            "Default follow settings",
            "Adult confirmation"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::site-preferences"
        }
      }
    }
  ]
}
---

# Save site preferences

## Trigger

A member wants to change what they see or who may reach them.

## Outcome

The preferences apply from the next page.

## Edge cases

- Default follow settings apply only to members followed afterwards.

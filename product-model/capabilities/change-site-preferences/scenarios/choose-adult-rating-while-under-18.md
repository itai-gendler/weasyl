---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses Mature as their maximum viewable rating and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::site-preferences"
        }
      }
    },
    {
      "text": "The birthday on the account makes the member under 18",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Birthday"
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
      "text": "The Product saves the other preferences on the account with General as the maximum viewable rating",
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
            "Default follow settings"
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

# Choose an adult rating while under 18

## Trigger

A member whose recorded birthday makes them under 18 chooses Mature or Explicit.

## Outcome

The maximum viewable rating stays General.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator enters search criteria",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Username",
            "Email address",
            "Joined at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::staff::user-search"
        }
      }
    }
  ]
}
---

# Search accounts

## Trigger

An administrator looks for related accounts.

## Outcome

The administrator sees up to 250 matching accounts with their email, standing and staff-note count.

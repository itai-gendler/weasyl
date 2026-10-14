---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member edits their profile information and saves",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Full name",
            "Catchphrase",
            "Profile text",
            "Profile details"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::profile-editor"
        }
      }
    },
    {
      "text": "The Product saves the profile information on the account",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Full name",
            "Catchphrase",
            "Profile text",
            "Profile details"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::profile-editor"
        }
      }
    }
  ]
}
---

# Save profile information

## Trigger

A member wants to change how their profile reads.

## Outcome

The profile shows the new information.

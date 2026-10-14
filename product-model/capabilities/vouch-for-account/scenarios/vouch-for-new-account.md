---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the unverified profile and chooses Vouch",
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
          "place": "web::community::profile"
        }
      }
    },
    {
      "text": "The Product marks the account verified by the member and emails its holder",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Verification"
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

# Vouch for a new account

## Trigger

A verified member visits the profile of an unverified account they know.

## Outcome

The account is verified and its holder is emailed that someone vouched for them.

## Edge cases

- Vouching for an account someone already vouched for changes nothing.
- People who are not staff see only a notice and the Vouch button on an unverified profile.

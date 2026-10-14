---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a current authenticator code or recovery code",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Two-factor authentication"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::two-factor-authentication"
        }
      }
    },
    {
      "text": "The Product turns off two-factor authentication for the account",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Two-factor authentication"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::two-factor-authentication"
        }
      }
    }
  ]
}
---

# Turn off two-factor authentication

## Trigger

A member no longer wants a second factor.

## Outcome

Sign-in asks only for the password again.

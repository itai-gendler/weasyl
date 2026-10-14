---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor enters the email address of their account",
      "kind": "actor",
      "actor": "visitor",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::password-reset"
        }
      }
    },
    {
      "text": "The Product emails a reset link valid for one hour to the address when an account uses it",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::password-reset"
        }
      }
    },
    {
      "text": "The Visitor opens the link and enters a new password long enough to be accepted",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::password-reset"
        }
      }
    },
    {
      "text": "The Product sets the new password on the account and ends its other sessions",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "facts": [
            "Password"
          ]
        },
        {
          "entity": "session",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::password-reset"
        }
      }
    }
  ]
}
---

# Reset a forgotten password

## Trigger

A person cannot remember their password.

## Outcome

The account has the new password, other sessions are signed out, and the person is invited to sign in.

## Edge cases

- An address with no account still gets an email saying so, and the page reads the same either way.
- Requesting a link passes a bot challenge.

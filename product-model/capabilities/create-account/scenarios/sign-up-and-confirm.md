---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor enters a username, email address and password and confirms being 13 or older",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::sign-up"
        }
      }
    },
    {
      "text": "The Product reserves the username in an unconfirmed account and emails a confirmation link",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "account",
          "effect": "creates",
          "to": "Unconfirmed",
          "facts": [
            "Username",
            "Email address",
            "Password",
            "Verification"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::sign-up"
        }
      }
    },
    {
      "text": "The Visitor opens the confirmation link",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public"
        }
      }
    },
    {
      "text": "The Product activates the account as unverified and offers sign-in",
      "kind": "product",
      "actor": "visitor",
      "entities": [
        {
          "entity": "account",
          "effect": "changes",
          "from": "Unconfirmed",
          "to": "Active",
          "facts": [
            "Joined at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public"
        }
      }
    }
  ]
}
---

# Sign up and confirm the account

## Trigger

A visitor wants a Weasyl account.

## Outcome

The account is active and the person may sign in; it stays unverified until someone vouches for it.

## Edge cases

- An unconfirmed account lapses two days after sign-up and its username becomes free again.
- Addresses at known disposable email domains are refused.
- Sign-up passes a bot challenge before anything is reserved.

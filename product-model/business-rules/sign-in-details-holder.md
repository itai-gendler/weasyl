---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Password",
        "Email address",
        "Two-factor authentication"
      ]
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "holds",
          "entity": "member"
        }
      ]
    },
    {
      "actors": [
        "visitor"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/profile.py#edit_email_password"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/resetpassword.py#reset"
    }
  ]
}
---

# Only the account holder changes the password, email address and second factor

A signed-in holder changes them in settings after giving the current password or a current code; someone not signed in changes only the password, and only through a reset link sent to the account's email address.

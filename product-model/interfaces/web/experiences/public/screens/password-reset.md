---
{
  "entities": [
    {
      "entity": "account",
      "shows": [
        "Username"
      ],
      "collects": [
        "Email address",
        "Password"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/etc/forgotpassword.html"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/etc/resetpassword.html"
    }
  ]
}
---

# Reset forgotten password

Where someone asks for a reset link and chooses a new password.

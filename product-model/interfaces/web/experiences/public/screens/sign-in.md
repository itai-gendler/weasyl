---
{
  "entities": [
    {
      "entity": "account",
      "collects": [
        "Username",
        "Password"
      ]
    },
    {
      "entity": "session",
      "collects": [
        "SFW mode"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/etc/signin.html"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/etc/signin_2fa_auth.html"
    }
  ]
}
---

# Sign in

Where people sign in with their username and password, and give a second factor when they use one.

---
{
  "entities": [
    {
      "entity": "account",
      "collects": [
        "Username",
        "Email address",
        "Password"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/etc/signup.html"
    }
  ]
}
---

# Sign up

Where a visitor creates an account and confirms it from the emailed link.

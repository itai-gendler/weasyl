---
{
  "availability": [
    {
      "place": "web::community"
    }
  ],
  "domain": "two-factor-authentication",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/two_factor_auth.py#tfa_disable_post_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/two_factor_auth.py#deactivate"
    }
  ]
}
---

# Disable two-factor authentication

A member turns two-factor authentication off by entering a current code or recovery code.

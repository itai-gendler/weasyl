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
      "target": "weasyl/controllers/two_factor_auth.py#tfa_init_verify_post_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/two_factor_auth.py#activate"
    }
  ]
}
---

# Enable two-factor authentication

A member turns on two-factor authentication by confirming their password, adding Weasyl to an authenticator app, saving recovery codes and entering a code.

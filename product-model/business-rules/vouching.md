---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Verification"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "member"
      ]
    },
    {
      "actors": [
        "moderator",
        "administrator",
        "director"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/user.py#vouch_"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "weasyl/templates/help/verification.html"
    }
  ]
}
---

# Verified members and staff vouch for accounts

A member may vouch only while their own account is verified. Vouching only ever moves an account from unverified to verified.

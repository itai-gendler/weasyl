---
{
  "entities": [
    {
      "entity": "staff-note",
      "shows": [
        "Content",
        "Written at"
      ],
      "collects": [
        "Content"
      ]
    },
    {
      "entity": "account",
      "shows": [
        "Username"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/profile.py#staffnotes_"
    }
  ]
}
---

# Staff notes

The staff notes kept about one account.

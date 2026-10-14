---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "journal",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "owns",
          "entity": "account"
        },
        {
          "verb": "holds",
          "entity": "member"
        }
      ],
      "when": [
        {
          "entity": "account",
          "fact": "Verification",
          "is": "Verified"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/content.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/config.py"
    }
  ]
}
---

# Only verified members post journals

The poster becomes the owner. Nothing can be posted while submissions are turned off for the whole site.

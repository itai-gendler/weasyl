---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "shout",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "writes",
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
      "target": "weasyl/shout.py#insert"
    }
  ]
}
---

# Only verified members shout, as the profile owner allows

The profile must be verified and not banned; its owner may take shouts from anyone, friends only or staff only. Staff may shout anywhere.

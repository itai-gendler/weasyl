---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Profile text",
        "Catchphrase",
        "Avatar"
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
      "target": "weasyl/moderation.py#editprofiletext"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/moderation.py#removeavatar"
    }
  ]
}
---

# Only the account holder or staff change the profile text, catchphrase and avatar

Moderators replace profile text or a catchphrase, or remove an avatar, that breaks the rules.

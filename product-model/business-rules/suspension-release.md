---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "from": "Suspended",
      "to": "Active"
    }
  ],
  "permits": [
    {
      "actors": [
        "moderator",
        "administrator",
        "director"
      ]
    },
    {
      "actors": [
        "visitor"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/moderation.py#setusermode"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/login.py#authenticate_bcrypt"
    }
  ]
}
---

# A suspension ends when staff release it or when its holder signs in after the release date

Staff may release a suspension at any time; otherwise it lifts itself the first time its holder signs in after the release date.

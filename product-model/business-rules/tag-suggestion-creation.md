---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "tag-suggestion",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "suggests",
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
        },
        {
          "entity": "account",
          "fact": "Tag suggestions allowed",
          "is": "Yes"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/searchtag.py#_set_suggested_tags"
    }
  ]
}
---

# Only verified members allowed to suggest tags suggest them

Administrators can turn suggesting off for an account. Tags matching the owner's or the global tagging restrictions are never added, and an owner who ignores the member refuses their suggestions.

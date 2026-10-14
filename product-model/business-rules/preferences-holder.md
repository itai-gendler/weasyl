---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Maximum viewable rating",
        "Adult confirmation",
        "Custom thumbnails",
        "Hidden from guests",
        "Statistics hidden",
        "Favorites hidden",
        "Shouts from",
        "Notes from",
        "Default follow settings",
        "Community tagging restrictions",
        "Collection requests allowed",
        "Collection notifications"
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
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/profile.py#edit_preferences"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/profile.py#set_collection_preferences"
    }
  ]
}
---

# Only the account holder changes their preferences

Site preferences, tagging restrictions and collection settings are the holder's alone.

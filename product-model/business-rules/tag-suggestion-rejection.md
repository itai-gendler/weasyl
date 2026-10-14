---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "tag-suggestion",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "has",
          "entity": "submission"
        },
        {
          "verb": "owns",
          "entity": "account"
        },
        {
          "verb": "holds",
          "entity": "member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "character"
        },
        {
          "verb": "owns",
          "entity": "account"
        },
        {
          "verb": "holds",
          "entity": "member"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "journal"
        },
        {
          "verb": "owns",
          "entity": "account"
        },
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
      "target": "weasyl/searchtag.py#suggestion_arbitrate"
    }
  ]
}
---

# Only the post's owner or staff reject a tag suggestion

A rejection can be undone for a short while.

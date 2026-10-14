---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "comment",
      "effect": "changes",
      "to": "Hidden"
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
      ]
    },
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
      "target": "weasyl/comment.py#remove"
    }
  ]
}
---

# The item's owner, staff, or the writer of a comment without visible replies hide a comment

Hidden comments and their replies stay visible to staff.

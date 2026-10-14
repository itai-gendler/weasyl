---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "submission",
      "effect": "changes",
      "facts": [
        "Submission file",
        "Cover art"
      ]
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
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/submission.py#reupload"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/submission.py#reupload_cover"
    }
  ]
}
---

# Only the owner replaces a submission's file or cover art

Staff may only remove cover art.

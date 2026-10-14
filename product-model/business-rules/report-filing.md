---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "report",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "files",
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
      "target": "weasyl/report.py#create"
    }
  ]
}
---

# Members report visible posts

Each violation is one that applies to the kind of post; some need a comment.

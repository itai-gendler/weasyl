---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "tag-filter",
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
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/blocktag.py#insert"
    }
  ]
}
---

# Only the member blocks tags for themself

A member may block from a rating only if their age allows that rating.

---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "submission"
    },
    {
      "type": "entity",
      "id": "character"
    },
    {
      "type": "entity",
      "id": "journal"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/frienduser.py#check"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/macro.py"
    }
  ]
}
---

# Friends-only posts are seen only by the owner and their friends

They never appear to visitors, in popular lists or as collections; notifications about them reach only friends.

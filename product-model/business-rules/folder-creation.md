---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "folder",
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
      "target": "weasyl/folder.py#create"
    }
  ]
}
---

# Members create folders only in their own gallery

Folders nest one level deep and sibling titles are unique.

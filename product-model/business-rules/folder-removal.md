---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "folder",
      "effect": "removes"
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
      "target": "weasyl/folder.py#remove"
    }
  ]
}
---

# Only the owner removes a folder

Its subfolders go with it and their submissions move to the root.

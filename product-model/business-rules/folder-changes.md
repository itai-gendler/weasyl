---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "folder",
      "effect": "changes"
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
      "target": "weasyl/folder.py#rename"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/folder.py#move"
    }
  ]
}
---

# Only the owner renames, moves or sets the options of a folder

Staff do not manage members' folders.

---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "character",
      "effect": "changes",
      "facts": [
        "Image"
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
      "target": "weasyl/character.py#reupload"
    }
  ]
}
---

# Only the owner replaces a character's image

Staff cannot replace a member's character image.

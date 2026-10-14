---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "tag-filter",
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
      "target": "weasyl/blocktag.py#remove_list"
    }
  ]
}
---

# Only the member unblocks their blocked tags

Tag filters are private to the member who keeps them.

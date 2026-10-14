---
{
  "relations": [
    {
      "entity": "comment",
      "verb": "has",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/siteupdate.py#create"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/siteupdate.py#edit"
    }
  ]
}
---

# Site update

A news post from Weasyl staff.

## Information kept

- **Title** — the update's title
- **Content** — the update's text
- **Posted as mascot** — whether it is attributed to the site mascot
- **Posted at** — when it was posted

---
{
  "relations": [
    {
      "entity": "comment",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "favorite",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "tag-suggestion",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "report",
      "verb": "is reported in",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/journal.py#create"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/journal.py#edit"
    }
  ]
}
---

# Journal

A written journal entry a member posts on their profile.

## Information kept

- **Title** — the journal's title
- **Content** — the entry's text
- **Rating** — General, Mature (18+) or Explicit (18+)
- **Tags** — the approved tags people search by
- **Friends only** — whether only the owner's friends may see it
- **Posted at** — when it was posted
- **Views** — how many times others have viewed it

## States

### Visible

Shown to everyone allowed to see it.

### Hidden

Removed by its owner or hidden by staff; only staff can still see it.

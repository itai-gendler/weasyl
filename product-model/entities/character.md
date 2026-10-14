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
      "target": "weasyl/character.py#create"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/character.py#edit"
    }
  ]
}
---

# Character

A character reference sheet a member posts: an image with the character's details.

## Information kept

- **Name** — the character's name
- **Age** — the character's stated age
- **Gender** — the character's gender
- **Height** — the character's height
- **Weight** — the character's weight
- **Species** — the character's species
- **Description** — the owner's description
- **Rating** — General, Mature (18+) or Explicit (18+)
- **Tags** — the approved tags people search by
- **Friends only** — whether only the owner's friends may see it
- **Image** — the reference image
- **Thumbnail** — the gallery thumbnail selected from the image
- **Posted at** — when it was posted
- **Views** — how many times others have viewed it

## States

### Visible

Shown to everyone allowed to see it.

### Hidden

Removed by its owner or hidden by staff; only staff can still see it.

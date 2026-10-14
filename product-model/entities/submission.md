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
      "entity": "collection",
      "verb": "is collected as",
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
      "target": "weasyl/submission.py#create_visual"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/submission.py#select_view"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "libweasyl/ratings.py"
    }
  ]
}
---

# Submission

A piece of visual art, writing or multimedia a member posts to their gallery.

## Information kept

- **Title** — the submission's title
- **Description** — the artist's description
- **Category** — Visual, Literary or Multimedia, with a subcategory such as Digital, Story or Original Music
- **Rating** — General, Mature (18+) or Explicit (18+)
- **Folder** — the gallery folder holding it, or the root
- **Tags** — the approved tags people search by
- **Friends only** — whether only the owner's friends may see it
- **Critique requested** — whether the artist asks for critique
- **Submission file** — the uploaded image, text, PDF, audio or Flash file
- **Cover art** — the image shown for literary and multimedia work, and the display copy of visual work
- **Thumbnail** — the gallery thumbnail, generated or chosen by the artist
- **Embedded media** — a linked Google Docs document or video/audio page shown in place of a file
- **Posted at** — when it was posted
- **Views** — how many times others have viewed it
- **Favorites** — how many people have favorited it

## States

### Visible

Shown in the gallery and to everyone allowed to see it.

### Hidden

Removed by its owner or hidden by staff; only staff can still see it.

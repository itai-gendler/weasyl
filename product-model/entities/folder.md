---
{
  "relations": [
    {
      "entity": "submission",
      "verb": "contains",
      "cardinality": "one-to-many"
    },
    {
      "entity": "folder",
      "verb": "contains subfolder",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/folder.py#create"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/folder.py#update_settings"
    }
  ]
}
---

# Folder

A gallery folder a member sorts their submissions into; folders nest one level deep.

## Information kept

- **Title** — the folder's name, unique among its siblings
- **Parent folder** — the top-level folder it sits in, or none
- **Featured** — whether a random submission from it is featured on the profile
- **Hidden from front page** — whether its submissions stay off the front page and browse lists
- **Hidden from profile** — whether its submissions stay off the profile page
- **No follower notifications** — whether new submissions in it skip follower notifications

---
{
  "entities": [
    {
      "entity": "submission",
      "collects": [
        "Title",
        "Description",
        "Category",
        "Rating",
        "Folder",
        "Tags",
        "Friends only",
        "Critique requested",
        "Submission file",
        "Cover art",
        "Thumbnail",
        "Embedded media"
      ]
    },
    {
      "entity": "folder",
      "shows": [
        "Title"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/submit/visual.html"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/submit/literary.html"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/submit/multimedia.html"
    }
  ]
}
---

# Submit artwork

Where a member uploads visual, literary or multimedia work.

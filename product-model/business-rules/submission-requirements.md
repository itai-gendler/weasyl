---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "submission",
      "effect": "creates",
      "facts": [
        "Title",
        "Rating",
        "Tags",
        "Submission file"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/submission.py#_create_submission"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/submission.py#check_for_duplicate_media"
    }
  ]
}
---

# A submission needs a title, a rating and at least two tags

Uploaded files are limited by type: images up to 50 MB, text up to 2 MB, PDF and HTML up to 10 MB, MP3 up to 15 MB, Flash up to 50 MB; thumbnails and covers up to 10 MB. A file identical to one of the owner's visible submissions is refused.

---
{
  "availability": [
    {
      "place": "web::community"
    }
  ],
  "domain": "submit",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/content.py#submit_visual_post_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/content.py#submit_literary_post_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/content.py#submit_multimedia_post_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/submission.py#create_literary"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/submission.py#create_multimedia"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/welcome.py#submission_insert"
    }
  ]
}
---

# Submit artwork

A verified member posts visual art, writing or multimedia with a title, category, rating, at least two tags and an optional folder, as an uploaded file or, for writing and multimedia, an embedded Google Docs document or media page. Followers are notified unless the member opts out or the folder is set not to notify.

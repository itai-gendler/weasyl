---
{
  "availability": [
    {
      "place": "web::public"
    },
    {
      "place": "web::community"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/detail.py#submission_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/submission.py#select_view"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/define.py#common_view_content"
    }
  ]
}
---

# View submission

Anyone opens a submission they are allowed to see. Visitors see General work; members see up to their maximum viewable rating, and their own work regardless unless in SFW mode. Work above that rating asks for confirmation first.

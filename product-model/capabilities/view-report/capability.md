---
{
  "availability": [
    {
      "place": "web::staff"
    }
  ],
  "domain": "moderation",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/report.py#select_view"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/moderation.py#modcontrol_report_"
    }
  ]
}
---

# View report

Staff open one report with the reported item, the owner's other reports and every report comment.

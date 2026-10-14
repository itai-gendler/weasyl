---
{
  "entities": [
    {
      "entity": "report",
      "shows": [
        "Reported item",
        "Violation",
        "Report comments",
        "Assigned moderator",
        "Closure reason",
        "Closure explanation",
        "Opened at"
      ],
      "collects": [
        "Report comments",
        "Closure reason",
        "Closure explanation"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/templates/modcontrol/report.html"
    }
  ]
}
---

# Report

One report with the reported item, related reports and every report comment.

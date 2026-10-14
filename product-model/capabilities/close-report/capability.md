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
      "target": "weasyl/report.py#close"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/moderation.py#modcontrol_closereport_"
    }
  ]
}
---

# Close report

A staff member closes a report as action taken, no action taken or invalid, with an explanation, optionally with all open reports against the same owner. Closing with action taken sends the owner a note and records it in their staff notes.

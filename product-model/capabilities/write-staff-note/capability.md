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
      "target": "weasyl/controllers/content.py#submit_shout_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/moderation.py#modcontrol_copynotetostaffnotes_post_"
    }
  ]
}
---

# Write staff note

Staff write a staff note about an account, or reply to one; a reply notifies the staff member replied to.

---
{
  "availability": [
    {
      "place": "web::staff"
    }
  ],
  "domain": "administration",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/admin.py#admincontrol_manageuser_post_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/profile.py#do_manage"
    }
  ]
}
---

# Edit account details

An administrator corrects an account's username, full name, catchphrase, birthday, gender, country and links, and turns tag suggestions off or on for it. Only directors manage other administrators.

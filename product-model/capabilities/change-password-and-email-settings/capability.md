---
{
  "availability": [
    {
      "place": "web::community"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/profile.py#edit_email_password"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/login.py#verify_email_change"
    }
  ]
}
---

# Change password and email settings

A member changes their password or email address after entering their current password. A new password signs out other sessions; a new address takes effect from the link emailed to it.

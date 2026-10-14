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
      "target": "weasyl/login.py#change_username"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/settings.py#control_username_post_"
    }
  ]
}
---

# Change username

A member changes their username at most once every 30 days; the former name keeps pointing to them until they release it. A change of capitalization alone is always allowed.

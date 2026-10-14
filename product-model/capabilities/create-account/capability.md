---
{
  "availability": [
    {
      "place": "web::public"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/user.py#signup_post_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/login.py#create"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/login.py#verify"
    }
  ]
}
---

# Create account

A visitor signs up with a username, email address and password and activates the account from the emailed confirmation link. A new account starts unverified.

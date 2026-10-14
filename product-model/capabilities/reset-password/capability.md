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
      "target": "weasyl/resetpassword.py#request"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/resetpassword.py#reset"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/user.py#resetpassword_post_"
    }
  ]
}
---

# Reset password

Someone who forgot their password asks for a reset link by email address and chooses a new password from it; every other session of the account ends.

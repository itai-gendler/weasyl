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
      "target": "weasyl/controllers/user.py#signin_post_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/user.py#signin_2fa_auth_post_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/login.py#authenticate_bcrypt"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/moderation.py#get_suspension_message"
    }
  ]
}
---

# Sign in

A person signs in with their username and password, giving an authenticator or recovery code when two-factor authentication is on. Suspended and banned accounts are turned away with the reason.

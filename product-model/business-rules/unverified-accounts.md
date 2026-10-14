---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/profile.py#profile_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/note.py#send"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/shout.py#insert"
    }
  ]
}
---

# Unverified accounts stay out of sight and cannot post or reach others

Until someone vouches for it, an account's profile is shown only to staff, and it cannot submit, comment, shout, tag, send notes, request friendship or collections, or receive shouts or notes.

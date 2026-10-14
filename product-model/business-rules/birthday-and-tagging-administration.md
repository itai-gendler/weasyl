---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "changes",
      "facts": [
        "Birthday",
        "Tag suggestions allowed"
      ]
    }
  ],
  "permits": [
    {
      "actors": [
        "administrator",
        "director"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/admin.py#admincontrol_manageuser_post_"
    }
  ]
}
---

# Only administrators record a birthday or turn off tag suggestions for an account

Directors do so for other administrators.

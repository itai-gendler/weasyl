---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "account",
      "effect": "removes"
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
      "target": "weasyl/controllers/admin.py#admincontrol_pending_accounts_post_"
    }
  ]
}
---

# Only administrators purge pending accounts

Purging frees the reserved username and address.

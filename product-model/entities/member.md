---
{
  "acts": "external",
  "kind": "person",
  "relations": [
    {
      "entity": "account",
      "verb": "holds",
      "cardinality": "one-to-one"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/decorators.py#login_required"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "libweasyl/staff.py#_init_staff"
    },
    {
      "kind": "code",
      "role": "context",
      "target": "config/weasyl-staff.example.py"
    }
  ]
}
---

# Member

A signed-in person sharing and following work on Weasyl. Every account holds this role; staff are members too.

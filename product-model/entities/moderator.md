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
      "target": "weasyl/controllers/decorators.py#moderator_only"
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

# Moderator

A staff member who handles reports, moderates posts and manages ordinary accounts. Administrators and directors hold every moderator power.

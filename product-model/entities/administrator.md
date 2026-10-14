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
      "target": "weasyl/controllers/decorators.py#admin_only"
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

# Administrator

A staff member who also posts site updates and manages account details and pending sign-ups. Directors hold every administrator power.

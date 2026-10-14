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
      "target": "weasyl/controllers/decorators.py#director_only"
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

# Director

The most senior staff role, which also sets the global community tagging restrictions and manages other administrators.

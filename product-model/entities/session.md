---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/sessions.py#create_session"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/define.py#is_sfw_mode"
    }
  ]
}
---

# Session

A signed-in browser's session.

## Information kept

- **SFW mode** — whether this browser shows only General-rated work regardless of the account's preference
- **Signed in at** — when the session began

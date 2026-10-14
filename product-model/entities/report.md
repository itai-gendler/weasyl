---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/report.py#create"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/report.py#close"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "libweasyl/models/content.py#Report"
    }
  ]
}
---

# Report

Members' reports about one submission, character or journal, handled by staff.

## Information kept

- **Reported item** — the submission, character or journal reported
- **Violation** — the rule each reporter says was broken
- **Report comments** — each reporter's or moderator's comment, with who wrote it and when
- **Assigned moderator** — the staff member reviewing or who closed it
- **Closure reason** — action taken, no action taken, or invalid
- **Closure explanation** — the staff explanation given on closing
- **Opened at** — when the first report arrived

## States

### Open

Waiting for staff.

### Under review

Assigned to a staff member.

### Closed

Handled.

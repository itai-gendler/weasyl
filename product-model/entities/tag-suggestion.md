---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/searchtag.py#_set_suggested_tags"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/searchtag.py#suggestion_arbitrate"
    }
  ]
}
---

# Tag suggestion

A tag someone other than the owner added to a post, waiting for the owner's approval.

## Information kept

- **Tag** — the suggested tag
- **Suggested by** — who suggested it

## States

### Suggested

Shown as a suggestion until the owner decides.

### Approved

Part of the post's tags.

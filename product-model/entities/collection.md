---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/collection.py#offer"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/collection.py#request"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/collection.py#pending_accept"
    }
  ]
}
---

# Collection

Another member's submission shown in a member's gallery as a collected piece, usually art made for or featuring them.

## Information kept

- **Collected at** — when the collection was offered, requested or accepted

## States

### Offered

The artist offered it; waiting for the collector.

### Requested

The collector asked for it; waiting for the artist.

### Accepted

Shown in the collector's collections.

---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "submission"
    },
    {
      "type": "entity",
      "id": "comment"
    },
    {
      "type": "entity",
      "id": "shout"
    },
    {
      "type": "entity",
      "id": "ignore-list-entry"
    },
    {
      "type": "entity",
      "id": "tag-filter"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/blocktag.py#check"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/ignoreuser.py#check"
    }
  ]
}
---

# People one ignores and tags one blocks stay out of one's view

Their posts, comments and shouts are filtered from browsing, searches, galleries and notifications; a single post may still be opened on purpose.

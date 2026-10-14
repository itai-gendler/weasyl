---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "submission"
    },
    {
      "type": "entity",
      "id": "character"
    },
    {
      "type": "entity",
      "id": "journal"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/define.py#get_rating"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/controllers/detail.py#submission_"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/welcome.py#submission_insert"
    },
    {
      "kind": "doc",
      "role": "intent",
      "target": "weasyl/templates/help/ratings.html"
    }
  ]
}
---

# Posts above a viewer's rating are withheld

Visitors and SFW mode see General only; members see up to their maximum viewable rating, and their own posts at any rating outside SFW mode. A single submission above the limit may be viewed after confirming age; characters and journals above it are refused. Followers are notified only of work they may see.

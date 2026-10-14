---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "staff-note"
    },
    {
      "type": "capability",
      "id": "hide-content"
    },
    {
      "type": "capability",
      "id": "show-content"
    },
    {
      "type": "capability",
      "id": "change-content-rating"
    },
    {
      "type": "capability",
      "id": "suspend-user"
    },
    {
      "type": "capability",
      "id": "ban-user"
    },
    {
      "type": "capability",
      "id": "release-user"
    },
    {
      "type": "capability",
      "id": "replace-profile-text"
    },
    {
      "type": "capability",
      "id": "remove-avatar"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/moderation.py#note_about"
    }
  ]
}
---

# Staff actions on an account or its posts are recorded in its staff notes

Hiding, showing, re-rating, editing posts, suspending, banning, releasing, replacing profile text and removing avatars each add a staff note about the affected account.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member opens the profile",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Username",
            "Full name",
            "Profile text",
            "Avatar"
          ]
        },
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Thumbnail"
          ]
        },
        {
          "entity": "shout",
          "effect": "reads",
          "facts": [
            "Content",
            "Posted at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::profile"
        }
      }
    }
  ]
}
---

# View a profile as a member

## Trigger

A member visits another member.

## Outcome

The member sees the profile with follow, friend, note and ignore actions.

## Edge cases

- The profile of an unverified account shows the member only a notice and, when the member is verified, a Vouch button.

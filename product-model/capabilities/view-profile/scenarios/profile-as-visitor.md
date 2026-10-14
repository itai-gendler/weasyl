---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens the profile",
      "kind": "actor",
      "actor": "visitor",
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
        }
      ],
      "contexts": {
        "web": {
          "place": "web::public::profile"
        }
      }
    }
  ]
}
---

# View a profile as a visitor

## Trigger

A visitor follows a link to an artist.

## Outcome

The visitor sees the profile and the artist's General work.

## Edge cases

- A profile its owner hides from people who are not signed in asks the visitor to sign in.
- Favorites the owner hides are not shown.

---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member writes a shout on a profile",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "shout",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::profile"
        }
      }
    },
    {
      "text": "The profile owner allows shouts only from staff, or only from friends and the member is not one",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Shouts from"
          ]
        },
        {
          "entity": "shout",
          "effect": "reads",
          "facts": []
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

# Shout where the owner allows only friends or staff

## Trigger

A member shouts on a profile that takes shouts only from friends or staff.

## Outcome

No shout is posted.

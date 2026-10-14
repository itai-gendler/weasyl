---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member chooses SFW on",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community"
        }
      }
    },
    {
      "text": "The Product turns on SFW mode for the session",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "session",
          "effect": "changes",
          "facts": [
            "SFW mode"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community"
        }
      }
    }
  ]
}
---

# Turn on SFW mode

## Trigger

A member is browsing somewhere only safe-for-work content should appear.

## Outcome

Only General-rated work is shown in this browser until SFW mode is turned off.

## Edge cases

- When the rating preference is General and the member has nothing above General, SFW mode is shown as always on.

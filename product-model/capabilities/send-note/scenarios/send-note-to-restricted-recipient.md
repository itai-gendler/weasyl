---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a recipient, a title and a message",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::note-composer"
        }
      }
    },
    {
      "text": "The recipient is unverified, ignores the member, or allows messages only from friends or staff and has never written to the member",
      "kind": "condition",
      "actor": "member",
      "entities": [
        {
          "entity": "account",
          "effect": "reads",
          "facts": [
            "Notes from",
            "Verification"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::note-composer"
        }
      }
    }
  ]
}
---

# Send a note to someone who does not accept it

## Trigger

A member writes to someone who takes notes only from friends or staff.

## Outcome

No note is sent and the recipient is reported as invalid.

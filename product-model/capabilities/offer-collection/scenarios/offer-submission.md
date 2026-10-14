---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters the username to offer their submission to",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-page"
        }
      }
    },
    {
      "text": "The Product creates the collection offer and notifies the recipient",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "collection",
          "effect": "creates",
          "to": "Offered",
          "facts": [
            "Collected at"
          ]
        },
        {
          "entity": "notification",
          "effect": "creates",
          "facts": [
            "Kind",
            "Sender",
            "Subject",
            "Received at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::submission-page"
        }
      }
    }
  ]
}
---

# Offer a submission as a collection

## Trigger

An artist made a piece for someone.

## Outcome

The other member has a pending collection offer.

## Edge cases

- Offering is refused when either member ignores the other or the submission is already collected or offered to that member.

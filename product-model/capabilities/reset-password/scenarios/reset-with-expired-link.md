---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Visitor opens an old reset link",
      "kind": "actor",
      "actor": "visitor",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::password-reset"
        }
      }
    },
    {
      "text": "The link is older than one hour or was already used",
      "kind": "condition",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::public::password-reset"
        }
      }
    }
  ]
}
---

# Follow an expired reset link

## Trigger

A person follows a reset link more than an hour old.

## Outcome

No password changes and the person is told the link may have expired.

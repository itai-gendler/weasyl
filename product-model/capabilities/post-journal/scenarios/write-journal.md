---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member writes a title, the entry, a rating and tags",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::journal-form"
        }
      }
    },
    {
      "text": "The Product creates the journal",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "journal",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Title",
            "Content",
            "Rating",
            "Tags",
            "Friends only",
            "Posted at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::journal-form"
        }
      }
    },
    {
      "text": "The Product notifies each follower whose Follow covers journals, whose rating preference allows it and who does not block its tags",
      "kind": "product",
      "entities": [
        {
          "entity": "follow",
          "effect": "reads",
          "facts": [
            "Notification kinds"
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
        },
        {
          "entity": "journal",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::journal-form"
        }
      }
    },
    {
      "text": "The new journal is shown on its page",
      "kind": "condition",
      "entities": [
        {
          "entity": "journal",
          "effect": "reads",
          "facts": [
            "Title",
            "Content"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::journal-page"
        }
      }
    }
  ]
}
---

# Post a journal entry

## Trigger

A verified member wants to share news or thoughts.

## Outcome

The journal is posted and the member is on its page.

## Edge cases

- A journal needs a title and content; tags are optional.

---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member enters a link to a supported media page, a title, category, rating and tags",
      "kind": "actor",
      "actor": "member",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web::community::artwork-form"
        }
      }
    },
    {
      "text": "The Product creates the multimedia submission embedding the media with its thumbnail",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "submission",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Title",
            "Description",
            "Category",
            "Rating",
            "Folder",
            "Tags",
            "Friends only",
            "Critique requested",
            "Embedded media",
            "Thumbnail",
            "Posted at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::artwork-form"
        }
      }
    },
    {
      "text": "The Product notifies each follower whose Follow covers submissions, whose rating preference allows it and who does not block its tags",
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
          "entity": "submission",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::artwork-form"
        }
      }
    },
    {
      "text": "The new submission is shown on its page",
      "kind": "condition",
      "entities": [
        {
          "entity": "submission",
          "effect": "reads",
          "facts": [
            "Title",
            "Embedded media"
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

# Submit multimedia from a media link

## Trigger

A verified member wants to share a video or song hosted elsewhere.

## Outcome

The submission embeds the media and, unless the member declined, uses the media page's thumbnail.

## Edge cases

- A link to an unsupported site is refused; when the media site cannot be reached, the member is asked to try again.

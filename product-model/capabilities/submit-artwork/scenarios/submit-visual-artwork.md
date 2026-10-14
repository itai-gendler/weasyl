---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member uploads an image and enters a title, category, rating, tags and folder",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "folder",
          "effect": "reads",
          "facts": [
            "Title"
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
      "text": "The Product creates the submission with a generated thumbnail and display copy",
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
            "Submission file",
            "Cover art",
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
            "Submission file"
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

# Submit visual artwork

## Trigger

A verified member wants to share a picture.

## Outcome

The submission is in the member's gallery and the member is on its page.

## Edge cases

- Choosing Mature or Explicit records that the member confirmed being 18 or older; a member whose birthday makes them under 18 cannot choose it.
- Images may be JPEG, PNG or GIF up to 50 MB; custom thumbnails and covers up to 10 MB.
- Choosing not to notify followers, or a folder set not to notify, sends no follower notifications.
- While submissions are turned off for the whole site, nothing can be posted.

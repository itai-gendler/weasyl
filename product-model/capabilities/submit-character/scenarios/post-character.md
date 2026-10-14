---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Member uploads the character image and enters its name, details, rating and tags",
      "kind": "actor",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::character-form"
        }
      }
    },
    {
      "text": "The Product creates the character",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
          "effect": "creates",
          "to": "Visible",
          "facts": [
            "Name",
            "Age",
            "Gender",
            "Height",
            "Weight",
            "Species",
            "Description",
            "Rating",
            "Tags",
            "Friends only",
            "Image",
            "Posted at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::character-form"
        }
      }
    },
    {
      "text": "The Product notifies each follower whose Follow covers characters, whose rating preference allows it and who does not block its tags",
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
          "entity": "character",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::character-form"
        }
      }
    },
    {
      "text": "The Product takes the Member to select the thumbnail of the character",
      "kind": "product",
      "actor": "member",
      "entities": [
        {
          "entity": "character",
          "effect": "reads",
          "facts": [
            "Thumbnail"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web::community::thumbnail-selection"
        }
      }
    }
  ]
}
---

# Submit a character

## Trigger

A verified member wants to share a character reference.

## Outcome

The character exists and the member is selecting its thumbnail.

## Edge cases

- Character images may be JPEG, PNG or GIF.

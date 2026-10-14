---
{
  "relations": [
    {
      "entity": "submission",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "character",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "journal",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "folder",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "favorite",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "comment",
      "verb": "writes",
      "cardinality": "one-to-many"
    },
    {
      "entity": "shout",
      "verb": "writes",
      "cardinality": "one-to-many"
    },
    {
      "entity": "shout",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "staff-note",
      "verb": "writes",
      "cardinality": "one-to-many"
    },
    {
      "entity": "staff-note",
      "verb": "is the subject of",
      "cardinality": "one-to-many"
    },
    {
      "entity": "follow",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "follow",
      "verb": "is followed through",
      "cardinality": "one-to-many"
    },
    {
      "entity": "friendship",
      "verb": "sends",
      "cardinality": "one-to-many"
    },
    {
      "entity": "friendship",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "ignore-list-entry",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "tag-filter",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "tag-suggestion",
      "verb": "suggests",
      "cardinality": "one-to-many"
    },
    {
      "entity": "notification",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "note",
      "verb": "sends",
      "cardinality": "one-to-many"
    },
    {
      "entity": "note",
      "verb": "receives",
      "cardinality": "one-to-many"
    },
    {
      "entity": "collection",
      "verb": "owns",
      "cardinality": "one-to-many"
    },
    {
      "entity": "report",
      "verb": "files",
      "cardinality": "one-to-many"
    },
    {
      "entity": "session",
      "verb": "owns",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/login.py#create"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/login.py#initial_profile"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "weasyl/profile.py#edit_preferences"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "libweasyl/models/tables.py"
    }
  ]
}
---

# Account

A person's Weasyl account and profile: who they are on the site, how they sign in, and the preferences that decide what they see and who may reach them.

## Information kept

- **Username** — the name shown on the profile and used to sign in; after a change the former name keeps pointing to the account until released
- **Full name** — the display name shown as the profile's title
- **Email address** — where account messages are sent; a new address takes effect only after its confirmation link is followed
- **Password** — the secret used to sign in, at least 10 characters
- **Two-factor authentication** — whether sign-in also needs an authenticator code or recovery code, and the recovery codes left
- **Verification** — Unverified or Verified: whether an established member or staff has vouched for the account
- **Birthday** — the date of birth staff recorded, which limits the ratings the person may use
- **Adult confirmation** — whether the person has confirmed they are 18 or older
- **Maximum viewable rating** — the highest rating, General, Mature or Explicit, the person chooses to see
- **Profile text** — the profile's description
- **Catchphrase** — the short line shown under the name
- **Avatar** — the profile picture
- **Profile details** — gender, country and links to the person's other sites
- **Hidden from guests** — whether the profile is shown only to signed-in people
- **Statistics hidden** — whether the profile statistics are hidden
- **Favorites hidden** — whether the person's favorites are hidden from other people
- **Shouts from** — who may shout on the profile: anyone, friends only or staff only
- **Notes from** — who may send the person notes: anyone, friends only or staff only
- **Default follow settings** — which kinds of activity a new follow notifies about
- **Custom thumbnails** — whether artists' custom thumbnails or only generated ones are shown for visual submissions
- **Community tagging restrictions** — tag patterns other people may not add to the person's posts
- **Tag suggestions allowed** — whether the person may suggest tags on other people's posts
- **Collection requests allowed** — whether others may request the person's submissions for their collections
- **Collection notifications** — whether the person is notified of favorites and comments on submissions they collected
- **Suspension** — the reason and release date of a temporary suspension
- **Ban reason** — the reason given for a permanent ban
- **Joined at** — when the account was created

## States

### Unconfirmed

Signed up, waiting for the emailed confirmation link; it lapses after two days.

### Active

Confirmed and able to sign in.

### Suspended

Unable to sign in until the release date.

### Banned

Permanently unable to sign in.

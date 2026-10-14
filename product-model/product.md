---
id: weasyl
summary: A social gallery where artists, writers and musicians share rated, tagged work, follow each other, favorite and comment, while staff moderate the community.
category: social-gallery
tags: [art, community, gallery]
authors:
  - name: Weasyl contributors
    url: https://github.com/Weasyl/weasyl
license: Apache-2.0
languages: [en]
limitations:
  - New accounts post, comment and message only after an established member or staff vouches for them.
  - Removing a post hides it; staff can still see and restore it.
  - Accounts cannot be deleted; people remove their posts and profile information instead.
  - Gallery folders nest only one level deep.
  - Staff roles are assigned in the site's configuration, outside the product.
references:
  - { kind: code, role: intent, target: README.md }
  - { kind: code, role: implementation, target: weasyl/controllers/routes.py }
  - { kind: doc, role: intent, target: weasyl/templates/help/about.html }
---

# Weasyl

Weasyl is a social gallery website. Members post visual art, writing and multimedia as submissions, along with character sheets and journals, each with a content rating and tags. Galleries are organized into folders. People follow artists to be notified of new work, favorite and comment on posts, shout on profiles, send private notes, become friends to share friends-only work, and collect submissions made for them.

What anyone sees is shaped by ratings, friends-only settings, ignore lists and blocked tags. New accounts are verified by another member vouching for them. Staff handle reports, hide and re-rate posts, suspend or ban accounts and keep staff notes; administrators also post site updates and manage accounts.

## Intent

Weasyl is "a social gallery website designed for artists, writers, musicians, and more to share their work with other artists and fans", seeking "to bring the creative world together in one easy to use, friendly, community website."

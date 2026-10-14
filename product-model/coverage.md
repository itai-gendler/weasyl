---
scope: "Product-facing web code at af866f49f3d90d7441efbdb2c1b3377c4da2d8c7: accounts, posts, social features, notifications, notes, collections, site updates and staff tools."
method: Static reading of routes, controllers, domain modules, models and templates; nothing was run.
covered:
  - description: Route table and web controllers for accounts, posts, social features, settings, moderation and administration.
    paths: [weasyl/controllers/]
  - description: Domain modules behind accounts, posts, tags, folders, favorites, comments, shouts, follows, friends, ignores, notifications, notes, collections, reports, moderation and site updates.
    paths: [weasyl/login.py, weasyl/resetpassword.py, weasyl/two_factor_auth.py, weasyl/profile.py, weasyl/define.py, weasyl/submission.py, weasyl/character.py, weasyl/journal.py, weasyl/searchtag.py, weasyl/blocktag.py, weasyl/folder.py, weasyl/favorite.py, weasyl/comment.py, weasyl/shout.py, weasyl/followuser.py, weasyl/frienduser.py, weasyl/ignoreuser.py, weasyl/welcome.py, weasyl/message.py, weasyl/note.py, weasyl/collection.py, weasyl/report.py, weasyl/moderation.py, weasyl/siteupdate.py, weasyl/search.py, weasyl/index.py, weasyl/thumbnail.py, weasyl/avatar.py, weasyl/macro.py, weasyl/sessions.py]
  - description: Shared models, ratings and staff role sets.
    paths: [libweasyl/models/, libweasyl/ratings.py, libweasyl/staff.py, weasyl/staff_config.py]
  - description: Page templates read for places, labels and what each page shows.
    paths: [weasyl/templates/]
exclusions:
  - description: Tests and fixtures.
    paths: [weasyl/test/, libweasyl/test/, libweasyl/models/test/, libweasyl/conftest.py]
  - description: Database migrations.
    paths: [libweasyl/alembic/]
  - description: Front-end assets, styles and their build.
    paths: [assets/, build.ts, build-css.ts, deno.json, deno.lock, design/]
  - description: Containers, deployment, CI and developer tooling.
    paths: [containers/, Dockerfile, docker-compose.yml, wzl, .github/, ci/, tools/, libpng/, etc/, gunicorn.conf.py, imagemagick-policy.xml]
  - description: Outbound request sandbox and metrics.
    paths: [netferret/, weasyl/metrics.py]
  - description: Static help, policy and staff pages.
    paths: [weasyl/controllers/info.py, weasyl/templates/help/]
unmapped:
  - description: Public JSON API, API keys and OAuth authorization with their documentation.
    paths: [weasyl/api.py, weasyl/controllers/api.py, libweasyl/models/api.py, weasyl-apidocs/, weasyl/templates/oauth2/]
  - description: Commission settings, prices and the marketplace search.
    paths: [weasyl/commishinfo.py, weasyl/controllers/marketplace.py]
  - description: Streaming status and the streaming page.
    paths: [weasyl/templates/control/edit_streaming.html, weasyl/templates/etc/streaming.html]
  - description: Username aliases for premium accounts, banners and the popular page.
    paths: [weasyl/useralias.py, weasyl/banner.py, weasyl/templates/etc/popular.html]
limitations:
  - description: Which external media sites embed, and what they return, depends on the providers.
    paths: [weasyl/embed.py]
  - description: The bot challenge on sign-up and password reset is decided by an external service.
    paths: [weasyl/turnstile.py]
---

# Coverage

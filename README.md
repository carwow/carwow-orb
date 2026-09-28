carwow-orb
===

[![carwow orb version](https://img.shields.io/badge/endpoint.svg?url=https://badges.circleci.io/orb/carwow/carwow-orb)](https://circleci.com/orbs/registry/orb/carwow/carwow-orb)

carwow's orb for CircleCI with handy snippets.


Release
---

To release a new version add to the commit message in the master branch one of:
  - [semver:major]
  - [semver:minor]
  - [semver:patch]


Commands for app pipelines
---

Shared by dealers_site, quotes_site and flatmin:

  - `skip_unless_changed`: ends a job successfully on a branch that changed none of the given paths.
  - `lint_result`: reports one linter that an earlier step ran, so one job can run them all and still show each one.
  - `restore_playwright_browser` / `save_playwright_browser`: caches the Playwright browsers per Playwright version.
  - `restore_rubocop_cache` / `save_rubocop_cache`: restores RuboCop's result cache everywhere, saves it on master only.
  - `bundle_install`: installs into vendor/bundle and drops the downloaded .gem archives.
  - `add_timings`: adds a logfmt file's fields to the job's Honeycomb event.

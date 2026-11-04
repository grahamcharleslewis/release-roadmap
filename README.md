# Release roadmap

Planned releases of an Android and iOS app. The release site reads the
`releases/` folder and shows each file as a card on its **Upcoming** page, in
the same style as past releases: one card per version, labelled with the
platforms it's planned for. Edits here appear on the site at its next scheduled build (within
about 6 hours), or straight away if the site's workflow is run manually.

> The releases in this repo are **example content** to show the format. Replace
> them with your real plans.

## One file per version

Each `.md` file in `releases/` is one planned version, for one or both apps.
Name files after the version (`1.12.md`, `1.12.1.md`): cards appear in version
order, soonest first. `README.md` and files starting with `_` are ignored, so
copy `releases/_template.md` to start a new one.

```markdown
---
title: Version 1.12
platform: Android, iPhone
target: December 2026
status: In progress
---

## What's planned

- Changes planned for both apps

## Android only

- Changes planned for Android only

## iPhone only

- Changes planned for iPhone only

## Details

Optional longer notes, links or screenshots, shown in a collapsed
"More details" section.
```

### Front matter

| Field | Required | Notes |
|---|---|---|
| `title` | Yes | Shown as the card heading, e.g. `Version 1.12` |
| `platform` | No | `Android, iPhone` when the apps are in sync, or one of them. A single platform shows an "Android only" / "iPhone only" label |
| `target` | No | Free text, e.g. `December 2026` or `Early 2027` |
| `status` | No | Free text. `In progress` is highlighted; anything else gets a neutral badge |

### Sections

All sections are optional. Leave out any you don't need.

- **What's planned**: changes for every platform in `platform`. Bullets before
  any heading count as this section too.
- **Android only** / **iPhone only**: changes for one app only, shown as
  separate lists under the shared ones. Headings and the `platform` field must
  use the platform names set in the release site's config (`Android` and
  `iPhone` in these examples; use `iOS` instead if that's what the site uses).
  "only" is optional.
- **Details**: anything else, rendered as markdown in a collapsed "More details"
  section. Any other heading also goes into the details.

## Examples in this repo

| File | Shows |
|---|---|
| `releases/1.12.md` | Both apps, with some platform-specific changes and details |
| `releases/1.12.1.md` | One app only (Android) |
| `releases/1.13.md` | Both apps, fully in sync |

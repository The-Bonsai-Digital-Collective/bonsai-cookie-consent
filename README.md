# Bonsai Digital Cookie Consent Video Embed - CookieScript

A WordPress plugin that replaces YouTube embeds with a consent-safe placeholder until CookieScript marketing consent is granted.

> **Status:** Stable  
> **Requires:** WordPress 5.8+ • PHP 7.4+ (8.x supported)

## What It Does

- Converts YouTube embeds to `youtube-nocookie`
- Adds CookieScript-compatible attributes:
  - `data-src`
  - `data-cookiecategory`
- Shows a consent placeholder before consent:
  - Thumbnail image
  - Darkened overlay
  - Centered consent message
  - Centered CTA link/button
- Automatically reveals the iframe when CookieScript loads the `src`

## Admin Settings

Path: **Settings > Cookie Video Consent**

- **Cookie category key**
  - CookieScript category key to assign to video embeds (default: `marketing`).
- **Default video background image URL**
  - If set, this overrides all YouTube thumbnails.
- **Consent text**
  - Overlay message shown before consent.
  - If left empty, plugin default is used.
- **Consent link URL (optional)**
  - If provided, CTA links to this URL.
  - If empty, CTA attempts to open CookieScript preferences popup.
- **Consent link label**
  - Text shown on CTA button.

## Requirements

- WordPress 6.0+
- PHP 7.4+
- CookieScript installed and active on the site

## GitHub Admin Updates

This plugin now follows the same update model as your maintenance plugin using `yahnis-elsts/plugin-update-checker`.

- Updater bootstrap is in the main plugin file.
- Composer dependency is in `composer.json`.
- Autoload path is `vendor/autoload.php`.

### Release Workflow

1. Commit plugin changes, including `vendor/` and `composer.lock`.
2. Bump `Version` in the main plugin file.
3. Create a GitHub Release.
4. Attach a release zip asset of the plugin folder.
5. WordPress admin update checks will detect the newer release.

### Repo URL

Default repository constant currently points to:

- `https://github.com/gakdesign/cookie-consent-video-embed-cookiescript`

If your final repository slug is different, update `CCVE_COOKIESCRIPT_GITHUB_REPOSITORY` in the main plugin file.

## Release Notes

See `CHANGELOG.md`.

## License

GPL-2.0+

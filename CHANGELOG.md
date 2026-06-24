# Changelog

All notable changes to this plugin are documented in this file.
This project adheres to [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [2.1.0] - 2026-06-24

### Added
- GitHub-based update checks via Plugin Update Checker (`yahnis-elsts/plugin-update-checker` v5.7).
- Composer setup for updater dependency (`composer.json`, `composer.lock`, `vendor/`).

### Changed
- Added `Update URI` header and updater bootstrap to main plugin file.

---

## [2.0.0] - 2026-06-24

### Added
- WordPress settings page at **Settings > Cookie Video Consent**.
- Configurable cookie category key (default: `marketing`).
- Configurable default background image URL to override YouTube thumbnails.
- Configurable consent text with fallback default.
- Configurable consent CTA URL and label.
- Consent placeholder UI with dark overlay and centered CTA.
- Frontend CSS and JS enqueued as versioned assets via `wp_enqueue_scripts`.
- Plugin settings passed to JS via `wp_localize_script`.

### Changed
- Refactored plugin from inline footer script to proper enqueued JS and CSS assets.
- Upgraded plugin header metadata and internal option handling.

### Security
- All settings fields sanitised on save and escaped on output.
- Settings page gated behind `manage_options` capability check.

---

## [1.7] - 2025-01-01

### Added
- Initial YouTube iframe CookieScript compatibility logic.

[2.1.0]: https://github.com/gakdesign/cookie-consent-video-embed-cookiescript/compare/v2.0.0...v2.1.0
[2.0.0]: https://github.com/gakdesign/cookie-consent-video-embed-cookiescript/compare/v1.7...v2.0.0
[1.7]: https://github.com/gakdesign/cookie-consent-video-embed-cookiescript/releases/tag/v1.7

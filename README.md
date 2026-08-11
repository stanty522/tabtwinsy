# Tabtwinsy — Same Tabs in Every Window

Arc-style cross-window tab sync for Chrome and Chromium browsers (built with [Dia](https://www.diabrowser.com) in mind). The same tabs and tab groups, mirrored live across every window. Open a new window and it's already populated.

**Install:** [Chrome Web Store](https://chromewebstore.google.com/detail/idphljlhhddadnmbnjfdmllgknfnbodn)

Everything runs locally in your browser. No servers, no network requests, no analytics — your tab data never leaves your device.

## Reporting bugs

This repo is the public issue tracker for Tabtwinsy. [Open an issue](../../issues) and include:

1. Your browser (Dia, Chrome, etc.) and Tabtwinsy version (visible on `chrome://extensions`)
2. What you did, what you expected, what happened instead
3. A screenshot if it helps

## Changelog

### 1.0.15 (in review)
- Closing a tab in one window now closes it in the other windows too (previously the mirror over-protected each window's active tab, so a cross-window close never propagated)
- Fixed tabs sometimes rearranging when closing a tab (same-site tabs, e.g. two YouTube videos, could be mistaken for each other by the matcher)
- Fixed tab groups created while the extension was paused being deleted when toggling it back on
- Known issue, still open: opening a favorite (Dia top-left) can still create a duplicate regular tab in other windows

### 1.0.14
- Fixed tab groups failing to migrate to new windows (redirected URLs missed their group slot)
- Fixed the Google Meet tab force-switching back during calls (the extension was interfering with Meet's picture-in-picture window)
- Fixed scrambled tab order when opening a new window

### 1.0.5
- Initial Chrome Web Store release

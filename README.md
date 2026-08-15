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

### 1.0.27
- Fixed windows that open blank never receiving your tabs. In Dia this showed up when moving a window between spaces: the window was mistaken for a picture-in-picture surface, skipped, and then stayed empty. Any window that ends up empty is now filled automatically.

### 1.0.26
- The listing is now localized (English, Spanish, Portuguese, French, German, Japanese, Korean)
- Fixed the extension being able to act in the moment right after the browser wakes it, even when switched off

### 1.0.25
- Fixed recently-closed tabs "resurrecting" into new windows (the browser keeps invisible windows holding old tabs; they are no longer treated as sync sources)
- Mass tab removal safety guard: no sync pass can delete a large fraction of a window's tabs unless you actually closed them yourself
- Renaming a tab group now propagates to other windows on Dia (groups are renamed in place)
- Group collapse/expand and renames propagate within ~1 minute even when the browser sends no events
- New-window population now retries if interrupted, and no longer trips the safety limiter on large windows

### 1.0.23
- Fixed tab groups failing to migrate to new windows, and scrambled tab order (redirected and same-site tabs are now matched correctly)
- Closing a tab in one window now closes it in the other windows too
- Fixed tab groups being deleted when toggling the extension back on
- Browser favorites (e.g. Dia's top-left favorites) no longer duplicate as regular tabs in other windows
- Fixed the Google Meet tab force-switching back during calls
- New in Options: a "Sites kept window-local" list you can review and edit

### 1.0.14
- Fixed tab groups failing to migrate to new windows (redirected URLs missed their group slot)
- Fixed the Google Meet tab force-switching back during calls (the extension was interfering with Meet's picture-in-picture window)
- Fixed scrambled tab order when opening a new window

### 1.0.5
- Initial Chrome Web Store release

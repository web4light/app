# Changelog

## v0.2.1

### Added

- Added `/skills reload` slash command in the composer palette to reload skills mid-session, with an inline transcript notice showing the updated skill count.
- Added a hover-to-reveal copy button to inbox item links
- Added an onboarding step for Business, Enterprise, and GHES users that detects when required Copilot preview features are not enabled and guides them to enable the necessary settings.
- Live progress is now shown while cloning a GitHub repository, with per-stage status (receiving objects, resolving deltas) and percentages streamed from git.
- Section editor qualifiers now support comma-separated multi-values (e.g. `repo:a,b,c`, `label:bug,docs`). Typing a comma after a value reopens the autocomplete with already-selected options filtered out.

### Changed

- My Work inbox filter tabs can now be reordered by dragging, and the "All" tab appears first by default.
- The "Archive sessions" button in the sidebar now shows the number of sessions that will be archived (e.g. "Archive 5 sessions" or "Archive 1 session").

### Fixed

- Browser preview theming now uses native OS appearance (macOS webview appearance, isolated Windows WebView2 profiles) instead of injecting scripts into the previewed page, preventing hydration mismatches in frameworks like Next.js. The theme toggle is hidden on Linux where native external theming is unsupported.
- Browser previews now retain their page state (URL, title, favicon) when switching panels or navigating away from a session.
- Fixed a bug where adding a new GitHub repository would briefly show the new workspace then redirect to the home page, hiding clone progress and any error dialogs.
- Fixed an issue on Windows where the app would become unresponsive to screen readers (NVDA) and voice control software after losing window focus.
- Fixed an issue on Windows where the browser preview could appear duplicated due to the native WebView2 surface being out of sync with the React placeholder.
- Fixed sidebar header controls overlapping main content at non-default zoom levels
- Fixed theme toggle not applying correctly in browser preview on Windows
- Fixed update error messages in Settings > General appearing as a second status line below the app version subtitle instead of replacing it
- Git error toasts for failed push, pull, and commit operations now show the actual git error message instead of the raw command arguments.
- Improved alignment and visual consistency across the Settings dialog: switch rows are now vertically centered; the account removal confirmation no longer shows a nested card or double border; MCP server action button spacing is consistent with the rest of the UI.
- Merge and auto-merge availability now correctly reflects GitHub's actual merge permissions, fixing cases where the merge button appeared disabled when it should have been enabled.

## v0.2.0

### Added

- Technical Preview for the GitHub app

# 051 - Modal Popup

A simple modal (popup) window built with plain HTML, CSS, and JavaScript. Demonstrates showing/hiding an overlay and handling multiple ways of closing it.

## Files
- `051-modal-popup.html` — everything (markup, styles, and script) in a single file. Just open it in a browser.

## Features
- **Open button** reveals a centered modal over a dimmed overlay.
- **Multiple ways to close it:**
  - Clicking the `×` button in the corner
  - Clicking the "Got it" confirm button
  - Clicking anywhere on the dark overlay outside the modal box
  - Pressing the `Escape` key
- **Smooth animation** — the overlay fades in/out and the modal box scales/slides into place using CSS `transition`.
- **Responsive** — the modal shrinks to fit smaller screens with side padding.

## How it works (JS fundamentals used)
| Concept | Where it's used |
|---|---|
| `document.getElementById` | Selecting the button, overlay, and modal elements |
| `classList.add` / `classList.remove` | Toggling the `.show` class to trigger CSS transitions |
| `addEventListener("click", ...)` | Wiring up the open/close buttons |
| Event target checking (`event.target === overlay`) | Making sure a click *inside* the modal doesn't close it, only clicks on the overlay background do |
| `addEventListener("keydown", ...)` | Listening for the `Escape` key globally |

## Try it yourself
- Add a second modal triggered by a different button.
- Disable the "click outside to close" behavior and see how the UX changes.
- Add a fade-out delay before the overlay is fully hidden.

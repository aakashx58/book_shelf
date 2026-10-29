# Leon Vasari — VHS filmography shelf

Single-file hero page (`index.html`): plain HTML, CSS and vanilla JS. No build step and no libraries.

## Run
Open `index.html` in a browser. It needs a network connection for the images (Higgsfield proxy) and fonts (Google Fonts).

## Controls
| Input | Action |
|---|---|
| Click spine / arrows / ← → | Change film |
| Decade tabs | Jump to that decade (shortest way round the loop) |
| Wheel / drag | Scrub the shelf, snaps to the nearest tape |
| Click cover / play ring / Enter | Open the detail page |
| Escape / Close | Back to the shelf |

## Structure
- **Media:** 4 transparent WebP sheets; each spine and cover is a CSS background crop (`SHEET`, `BOX` in the script).
- **Shelf:** 12 films × 3 copies = 36 tapes in a CSS 3D stage; one `requestAnimationFrame` loop drives the spring scroll, the open and turn, the hover lift and the cursor tilt.
- **Caption and detail:** Web Animations API mask slides, a clip-path sheet open, and an SVG displacement-mask ink reveal for the poster. No opacity fades and no CSS keyframes.
- **Responsive** at 767px and below. `prefers-reduced-motion` makes everything instant.

## Not done
- Fonts are linked rather than embedded as base64.

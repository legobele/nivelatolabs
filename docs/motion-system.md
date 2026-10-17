# Motion system (mirror)

Short mirror of the motion section in the app repo's
DESIGN_SYSTEM_LABS.md, which is the canonical home. Giulia's
rule: zero jump-cuts, on the site and in the app.

Tokens (identical names/values in both repos):

- `--niv-mo-ease: cubic-bezier(.22, 1, .36, 1)` — the one easing family.
- `--niv-mo-micro: 160ms` — hover, press, focus, chevrons.
- `--niv-mo-view: 300ms` — menu/panel/modal transitions, both directions.
- `--niv-mo-enter: 560ms` — hero rise and scroll reveals.
- Entrances rise 26px on the site (10px in the app), fade from opacity 0.

Rules: entrances are keyframe-based and never gate content
visibility (no-JS still shows everything; the reveal system
only hides under `html.js`). Everything collapses under
`prefers-reduced-motion`. The scroll cue's fade should adopt
these tokens when next touched (it currently runs 450ms ease).

On this site the system is applied as one motion block before
`</head>` on every page: hero rise + reveal unification, the
variant menu open/close with content rise, the language
selector expand, and button/link micro transitions with
press feedback. Deferred: menu content exit animation (needs
a closing-state class in the menu JS; the overlay fade covers
close) and number tweens (JS counters; this system is CSS
only).

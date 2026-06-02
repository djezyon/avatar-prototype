# Design collaboration checklist

Use this when the goal is **exact visual fidelity**, not an approximate match.

## Before implementation

- **One source of truth** — Pick a single reference for this change (one Figma frame, one PNG, or one written spec). Avoid mixing an old screenshot with an older build.
- **Scope the component** — Name the exact UI piece (for example: “Makeup tray → Regional / Full Face segmented control”) so styling stays isolated and does not accidentally reuse unrelated styles.
- **Numbers beat inference** — List what you can: height, horizontal padding, gap between segments, corner radius, border (width + color), active vs inactive fills, text color, font size + weight, shadow (offset, blur, spread, opacity).

## Visual references

- **Screenshot** — Good for layout and hierarchy; treat fine detail (radius, 1px vs 2px borders) as **unconfirmed** unless you also provide inspect values or explicit numbers.
- **Figma inspect / design tokens** — Prefer copied CSS or token names for anything that must match pixel-for-pixel.
- **Assets** — For icons or non-standard shapes, provide SVG or exported PNG slices so nothing is redrawn from memory.

## Acceptance

- **Same viewport width** — Compare the implementation at the tray or canvas width you care about.
- **States** — Confirm default + active at minimum; include hover, focus, or disabled if the design depends on them.
- **Side-by-side or overlay** — Quick pass to catch “wrong component” issues before debating subjective taste.

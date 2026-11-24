---
name: stage-ios-screens
description: Stages 3 to 5 realistic iOS app screens inside iPhone frames on a clean presentation canvas, using Apple Human Interface guidelines and award-level craft. Use when designing iOS app screens, mobile app UI, iPhone mockups, a multi-screen app flow, or a Dribbble-style presentation of an iPhone app.
license: MIT
---

# stage-ios-screens

Design iOS app screens the way a senior product designer would ship a high-end iPhone app: Apple Human Interface craft, one accent, believable data, and a presentation that is already a screenshot.

This skill is only for native-feeling iOS app interfaces in device frames. Do not use it to design marketing websites, landing pages, scroll-driven campaign sites, or desktop web apps.

When picking structure and tone, open `references/app-archetypes.md`. When building chrome and type, follow `references/ios-components.md` exactly. Before finishing, audit against `references/banned-patterns.md`.

## 1. Confirm the job, then name the app

If the user has not said what the app is for, ask one short question and wait. Do not ask about colors, typography, or screen count.

If the purpose is clear, do not ask. Invent a short fictional app name: one or two words, a real word or a quiet coinage. Do not use -ly, -ify, -ai, -hub, or -app suffixes, and do not copy a well-known app's name. State the name, the accent color, and the screen list in one compact card, then build:

```
App: [name]
Job: [one line]
Accent: [hex]
Screens: [3 to 5 screen names, in flow order]
```

## 2. What to ship

Ship a single self-contained HTML file. The first view must be screenshot-ready: 3 to 5 iPhone frames in a single row on a clean presentation canvas.

Canvas and devices (see `references/ios-components.md` for exact measurements):

- Each screen is 390×844 logical points, inside a realistic iPhone frame with Dynamic Island, a status bar (time 9:41), and a home indicator.
- Sit the devices in one row, even gaps, a quiet studio ground, and a soft device shadow. No gradient backdrop, no typographic poster, no mock browser chrome.
- Scale the whole stage to fit the viewport. Do not wrap phones onto a second row.
- Optional quiet labels under each phone (app 13pt / Footnote). They must not compete with the UI.
- Light or dark should follow the archetype. Put a discreet canvas control that switches every device between light and dark, using the paired palettes, not a simple invert.

The 3 to 5 screens must read as one product flow, not as isolated widgets. Typical set: a home or list, a detail, a compose or sheet, and, when it is natural, an empty, loading, or error state. Do not force a junk empty screen if the story does not need one. If you include a sheet, show it in a real detent over a dimmed previous screen, not as a standalone rectangle.

Optional prototype: taps can move through the flow (tab changes, row push, sheet present, back). Use iOS-like motion from `references/ios-components.md`. The static first frame must still stand alone as a shot if nobody taps.

## 3. Visual rules

Follow `references/ios-components.md` for type, bars, safe areas, materials, icons, and spacing. Non-negotiable:

- 8pt grid. Content stays inside safe areas. Interactive controls are at least 44×44 pt.
- Type is the system / SF Pro stack with Inter as the fallback, at Dynamic Type sizes. Do not load a display serif or a third family for headlines.
- One accent color, used for tints, active tabs, and primary actions. System red, green, and orange are only for destructive, success, and warning. Pick an accent that fits the job; do not default to purple or indigo.
- Real navigation bars and tab bars (3 to 5 tabs when the app has a tab root). Icons are consistent-stroke inline SVGs in the SF Symbols manner. No emoji icons.
- Believable data only: specific names, irregular amounts, real-feeling times, merchants, places, and statuses. No lorem ipsum, no "John Doe", no "User", no $99 or 10,000 even totals.
- Copy is short and direct, like a shipped Apple app. No onboarding voice on standard screens.

If a needed fact is missing (a city, a price, a date), invent a coherent fictional one and stay consistent across screens. Do not invent legal claims, medical advice, or real-person identities.

## 4. Finish checklist

Copy this list and tick it before delivering:

- [ ] Purpose was clear, or one question was asked; app name and accent declared
- [ ] One HTML file; 3 to 5 phones in a single scaled row; 390×844; island, 9:41, home indicator
- [ ] Screens form a flow; chrome is real iOS (nav, tabs, sheets/detents if used)
- [ ] 8pt grid, 44pt targets, safe areas, system type scale, one accent
- [ ] SVG icons are consistent; data looks real; no banned patterns
- [ ] Light and dark both work; reduced-motion path is sane
- [ ] Screenshot is clean at first paint, with or without taps

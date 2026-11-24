# stage-ios-screens

A Gemini skill for iOS app screens that look like a real, high-end iPhone app.

It stages 3 to 5 screens in realistic iPhone frames (390×844, Dynamic Island, status bar, home indicator) on a clean presentation canvas, so one prompt can produce a screenshot-ready shot. Chrome follows Apple’s Human Interface guidelines: system typography, an 8pt grid, real navigation and tab bars, sheets and detents, and one accent color. Data is invented but believable. It is not a website or landing-page skill.

## Install in the Gemini app

Works in the Gemini app on the web (gemini.google.com), on Mac, and on mobile.

1. Download this folder, or download a zip that has `SKILL.md` in its main folder.
2. Open Gemini and go to **Customize → Skills**.
3. Click **Create**, then **Upload**.
4. Select this folder, or the `.zip`.
5. Review the name, description, and instructions, then click **Create**.

To use it, ask Gemini to design iOS app screens (or @mention `stage-ios-screens`). It should declare the app name and accent, then return a single HTML file. Open that file and screenshot the row of devices.

You can also create the skill manually: **Create manually**, then paste the name and description from `SKILL.md`, and paste the instructions (everything below the second `---`). If you go that route, also add the files in `references/` so the specs travel with the skill.

## Demo prompts

Run these after the skill is installed. The first one is the strongest screenshot.

1. `Design iOS screens for a flight tracker. The main trip is Wizz Air W6 402, Skopje (SKP) to London Luton (LTN), delayed 22 minutes, departing 14:10, gate B12. Show the live flight, the trip timeline, and the delay details.`

2. `Design iOS screens for a personal spending app. It's Thursday 19 Nov 2026 and I want this week in Lisbon: cafes, a metro card top-up, a museum ticket, and a transfer. Show home, a transaction detail, and a week chart that actually has axes.`

3. `Design iOS screens for a manual camera app at a serious-photographer level. Dark mode. Show the viewfinder with real exposure controls, a photo review, and a format or RAW settings sheet.`

If you already have an app name or an accent, include it in the prompt. Otherwise the skill will invent a short name and pick one accent.

## What’s in this repo

- `SKILL.md` — the skill (name, description, and instructions)
- `references/ios-components.md` — device frame, type scale, bars, sheets, icons, motion
- `references/app-archetypes.md` — how top apps in each category are structured
- `references/banned-patterns.md` — AI-app UI tells to reject before delivery

## License

MIT. See `LICENSE`.

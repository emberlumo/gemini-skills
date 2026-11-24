# iOS components

Use these measurements in logical points. The presentation device is 390×844 with a Dynamic Island, even though that mixes a familiar canvas size with current island hardware. Keep every screen on this size so the row lines up.

## Device frame

- Screen: 390×844, screen corner radius 47. Device bezel 12, outer radius 55, bezel color `#000000`.
- Dynamic Island: 126×37, radius 19, black, horizontally centered, top offset 11 from the screen edge. Do not draw a notch or a simple punch-hole.
- Status bar sits around the island, height included in the top safe area of 59. Time is **9:41**, leading, 15pt semibold, the label color of the current mode. Trailing: cellular, Wi-Fi, and battery in accurate iOS-like glyphs (not letters or emoji), same optical size.
- Home indicator: 134×5, radius 2.5, centered, 8 from the bottom edge. Light mode: `rgba(0,0,0,0.85)` on light screens, white on dark screens and on image-heavy heroes. Bottom safe area is 34.
- Device shadow on the canvas: `0 24px 48px rgba(0,0,0,0.18)`, no colored glow.
- Canvas ground: light `#E8E8ED`, dark presentation `#0B0B0C`. Side and vertical padding at least 48. Gap between devices 28. Scale the whole stage with `transform` so all phones stay on one row.

## Type

Font stack, in this order: `-apple-system, BlinkMacSystemFont, "SF Pro Display", "SF Pro Text", Inter, system-ui, sans-serif`. Use Display-like weight and tracking on Title 3 and up; Text-like tracking on Headline and smaller. Load Inter from Google Fonts only as a fallback (`400`, `500`, `600`, `700`). Do not add another family.

Default (Large) Dynamic Type. Do not invent in-between sizes.

| Style | Size | Weight | Line height | Tracking |
|---|---|---|---|---|
| Large Title | 34 | 700 | 41 | 0.4 |
| Title 1 | 28 | 700 | 34 | 0.36 |
| Title 2 | 22 | 700 | 28 | 0.35 |
| Title 3 | 20 | 600 | 25 | 0.38 |
| Headline | 17 | 600 | 22 | -0.41 |
| Body | 17 | 400 | 22 | -0.41 |
| Callout | 16 | 400 | 21 | -0.32 |
| Subhead | 15 | 400 | 20 | -0.24 |
| Footnote | 13 | 400 | 18 | -0.08 |
| Caption 1 | 12 | 400 | 16 | 0 |
| Caption 2 | 11 | 400 | 13 | 0.07 |
| Tab label | 10 | 500 | 12 | 0.06 |

Large titles are left-aligned on root list screens. Detail screens use a compact 17pt semibold title. Do not center body copy. Do not use type smaller than Caption 1 in the interface, except the 10pt tab label.

## Color and materials

Light:

- Label `#000000`, secondary `rgba(60,60,67,0.60)`, tertiary `rgba(60,60,67,0.30)`
- Background `#FFFFFF`, grouped / secondary `#F2F2F7`, elevated / tertiary `#FFFFFF`
- Separator `rgba(60,60,67,0.29)`
- Fill (controls) `rgba(120,120,128,0.16)`
- System red `#FF3B30`, green `#34C759`, orange `#FF9500`, yellow `#FFCC00`

Dark (do not invert the light palette):

- Label `#FFFFFF`, secondary `rgba(235,235,245,0.60)`, tertiary `rgba(235,235,245,0.30)`
- Background `#000000`, grouped / secondary `#1C1C1E`, elevated / tertiary `#2C2C2E`
- Separator `rgba(84,84,88,0.65)`
- Fill `rgba(120,120,128,0.24)`
- Semantic colors slightly brighter if contrast needs it: red `#FF453A`, green `#30D158`, orange `#FF9F0A`

Accent: one hex, declared in the app card. Active tabs, tints, progress, and the primary button use this color. In dark mode, lighten it just enough to keep contrast on `#1C1C1E` and `#000000`. Links and bar buttons use the accent, not system blue, unless the accent is system blue.

Materials: nav bars, tab bars, and the background behind a sheet use a blur (`backdrop-filter: saturate(180%) blur(20px)`) with a translucent fill (`rgba(255,255,255,0.72)` light, `rgba(30,30,30,0.72)` dark). Do not frost every card. Hairlines are 0.5px (1px at 1x is acceptable if 0.5px is uneven).

## Navigation bar

- Compact bar: 44 high, plus the 59 top safe area. Trailing and leading items sit on the 44pt row, 16 from the leading/trailing edges, 44×44 hit areas.
- Back control: a 17pt accent chevron, optionally followed by the previous title in 17pt. No hamburger menus on iPhone.
- Large-title mode: compact bar stays on top; the 34pt title sits in the content, 16 from the leading edge, 8 below the bar, 8 above the first collection.
- No bottom hairline unless content is scrolling under the bar. Bar buttons are 17pt Headline or 22×22 symbols, accent-colored, never pill-shaped capsules unless they are a genuine `UIMenu` or filter chip in content.

## Tab bar

- Use a tab root when the app has two or more primary destinations. 3 to 5 tabs, never 2, never 6.
- Bar height 49 plus the 34 home-indicator inset. Icons 25×25 in a 44×44 target, label 10pt under the icon, 2pt gap. Selected: filled symbol + accent. Unselected: outline symbol + secondary or tertiary label.
- The tab bar is a material. It does not float as a rounded capsule in the middle of the screen unless you are deliberately echoing that one current system pattern, and even then only on a single root, with correct safe-area padding.

## Lists, buttons, fields

- Inset grouped lists: 16 side inset on the canvas, group corner radius 10, 16pt content indent, separators indented to the text origin (not across icons). Min row height 44; subtitle rows 60–72; value rows can go to 88 if needed. Background is grouped; cells are elevated.
- Plain lists may go edge to edge on data-dense apps (mail, chat, flights). Keep separator insets consistent.
- Primary buttons: 50 tall, 12–14 radius, accent fill, 17pt semibold, 16 side margin. Destructive actions use system red. Do not make every row a full-width button.
- Text fields: 16pt Body, 12pt title or none, 36–44 high, correct keyboard type implied by the content (no fake keyboards unless a screen is about composing and you need the keyboard in the shot).
- Toggles, steppers, and segmented controls should look like system controls, not custom gummy switches.

## Sheets and detents

- Present from the bottom. Top corner radius 38. A grabber 36×5, radius 2.5, `rgba(60,60,67,0.30)` (light) or `rgba(235,235,245,0.30)` (dark), 5pt below the sheet top, centered.
- Medium detent: about 52% of the screen height. Large detent: the sheet sits 10pt below the top safe area. The dimming scrim is `rgba(0,0,0,0.38)`. The parent screen stays visible and slightly scaled (0.92) only on large detent, with rounded, clipped edges.
- Sheet content has its own compact nav or a leading Close / trailing Done in accent. It must not look like a card floating in the canvas.

## Icons

Inline SVG, 24×24 viewBox (22×22 optical if needed), stroke 1.6, round caps and joins, `currentColor`. Selected tab icons are filled (`fill` + no stroke, or a filled path). One optical size in bars, one slightly smaller in list leading icons (20). Align to the 8pt grid. No emoji, no brand logos unless the screen is literally about that brand, no random icon sets mixed with this stroke language.

## Motion

- Push: 350ms, `cubic-bezier(0.2, 0.8, 0.2, 1)`, incoming screen from the right, outgoing eases left about 30%.
- Sheet: 420ms, same curve, translates from the bottom; scrim fades.
- Tab change: cross-fade 200ms, no slide.
- Buttons and toggles: 120–180ms on highlight and value change.
- `@media (prefers-reduced-motion: reduce)`: no position travel, instant or 1ms fades only. Content must already be visible.

If you add a tappable prototype, hook up back, tabs, one row-to-detail, and one sheet at minimum. Leave a short HTML comment on each screen with any micro-interaction that is not obvious (`<!-- motion: checkmark springs to 1.08, then settles -->`).

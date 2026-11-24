# App archetypes

Pick the closest archetype and follow what the best iPhone apps in that category actually do. Do not mix a finance home with social-feed chrome, and do not fall back to a generic dashboard of four stat tiles.

## Productivity

References in spirit: Things, Linear’s iPhone app, Reminders, Craft.

- Information architecture is lists and dates, not a control panel. Home is Today, Inbox, a project, or a queue. Large titles. Project or tag color is a small tint, not a background.
- Rows: a 22pt checkbox or state mark, a Body title, a Footnote meta line (Tue 9:30, Project, priority). Incomplete work sits with complete work only when the product is a log; otherwise completed items collapse or leave.
- Compose is a sheet or a focused new-item screen with a keyboard-first layout, not a settings form.
- Empty state is calm and specific: “Nothing due today.” plus one action. No mascot parade.
- Accent is usually a single strong ink (Things red, Linear indigo-adjacent but you must pick a non-generic custom hex if you go cool-blue, and never a purple glow). Light mode is the default unless the user asked for dark.

## Finance

References in spirit: Revolut, Apple Card, Monzo, Copilot.

- The hero is one number (balance, spent this week, due) in Large Title or Title 1, with a Footnote period (“18–24 Nov”). Not four identical metric cards.
- The body is a transaction list: merchant, exact time, category, irregular amounts (`£14.60`, `$47.83`, `2.400 MKD`). Group by day. Leading marks can be a simple monogram or a category glyph, never a neon logo wall.
- Cards look like cards if they exist (aspect, type, last four digits). Spending charts, if used, have axes, units, and labeled dates. One series, not a rainbow doughnut.
- Dark often fits. Green and red are reserved for money in and money out, not for decoration.
- Error and delay states matter: “Couldn’t refresh HSBC · 20s ago” with Retry, not a blank hole.

## Travel

References in spirit: Flighty, Airbnb, App in the Air.

- Flights: typography is the interface. Airline and flight number, route (`SKP` → `LTN`), times in the local zone, terminal and gate, a delay stated in minutes. A quiet route graphic beats a decorative world map. Status (On time, Delayed 22m, Boarding, Landed) is typographic and color-coded with semantic colors, not a rainbow badge set.
- Stays: photography first, then place, dates, and a real price (`€187` for 2 nights, not `$99/night`). Photos must be generated or CSS/SVG placeholders that feel composed; never invented Unsplash URLs. Filters and maps are tools, not a homepage of categories.
- A useful third screen is a timeline, a boarding details sheet, a trip itinerary, or a reservation detail, not a profile tab full of settings.
- Data must be internally consistent (departure, duration, arrival, time zones).

## Social

References in spirit: a small, calm network, not a cloned Instagram or TikTok.

- A feed is typography, names, timestamps, and a few images at most. Real first and last names, or plausible usernames, and relative times that vary (`2m`, `47m`, `Yesterday`). Avoid a wall of heart counts.
- Composition is usually a text field or a short camera sheet, not a studio of filters.
- Profile is sparse: a name, a short line, a few posts. No “Welcome back” header, no streak fireworks, no follow-grid of circular avatars as the entire screen.
- If the product is chat, use message bubbles with system-like materials, timestamps on a cadence, and a composer pinned above the tab bar or keyboard. Delivery states are quiet.

## Fitness

References in spirit: a serious training log (Strength, Hevy, a focused run app), not a copy of Activity rings unless the app is actually about rings.

- Home is today’s session or the training calendar, not four rings plus a medal. Workouts show exercise, sets, weight, and rest with irregular numbers (`3×7 at 62.5 kg`, `5.42 km`, `4:48 /km`, `6h 12m sleep`).
- A session screen is a live or rest-state list: the current set highlighted, rest as a Title 1 timer, previous performance in Footnote.
- Charts have axes and units (kg, km, minutes). Empty week: “No sessions logged this week.” with Log a session.
- Light or dark both work; many training apps are dark. Keep the accent athletic and specific (a lime, a flame red, a steel blue), not gradient coral.

## Health

References in spirit: Health, a careful symptom or medication log. Clinical and calm.

- Privacy-first copy. No coachy exclamation. Home might be a morning summary or a log list, with units on every number (`117/74 mmHg`, `6h 12m`, `0.5 mg`).
- Charts always have axes, a date range, and a source line (“From Omron, 7 days”). One accent, one series unless comparison is the point.
- Medication and reminder screens are lists with schedules, remaining doses, and a clear Taken action. Errors are serious and plain: “Couldn’t sync last reading.”
- Prefer light mode. Avoid tropes of purple wellness gradients, leaf watermarks, and meditation-app blobs.

## Cross-cutting

- Every archetype still uses real iOS chrome from `references/ios-components.md`. A “unique” custom tab bar is not a substitute for craft.
- Settings, if shown at all, is a last screen, not one of the three hero shots.
- Dark mode is a paired palette, not a filter. Test typography contrast in both.

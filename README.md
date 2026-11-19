# Rec2Go Redesign

**A human-centered redesign of Rec2Go, the Rutgers Recreation app, built around the few quick tasks students actually open it for: getting in, checking what's open, and joining a class.**

Final project for an interaction design studio course at Rutgers University (Fall 2026). Status: research under way; student survey open, clickable prototype v1 built, usability testing planned.

**Live site:** https://anushka02singh.github.io/rec2go-redesign/ · **Survey:** https://anushka02singh.github.io/rec2go-redesign/survey/

---

## The problem

Students open Rec2Go for a few time-sensitive tasks, but the app follows the rec department's structure:

- **9 of 19** home tiles leave the app for web pages in a different visual style.
- Facility hours are split across **4 campus screens**, with no "open now" status or activity filter.
- The member pass sits behind an unexplained "NetID / Local" choice, and the boldest button on that screen is "Clear Barcode."
- A promo banner appears on almost every screen. One student said it makes the app "feel like a cheap mobile game."

## Project parts

| Part | What it is |
|---|---|
| **Part 1: AI wireframing critique** | Figma Make and Google Stitch given the same prompts in three rounds, then critiqued. Both assumed a single building and named the user "Jordan" when given no context, and both invented facility details that contradicted the real schedule. |
| **Part 2: HCD redesign** | Empathize → Define → Ideate → Prototype → Test, documented below. |

## What is in this repository

```
rec2go-redesign/
├── index.html            Project page (GitHub Pages)
├── survey/
│   └── index.html        Anonymous student survey, self-contained, no build step
├── figma-plugin/         Generates the clickable prototype in Figma
│   ├── manifest.json
│   ├── code.js
│   └── README.md
├── figures/
│   └── rec2go_v1_screens.png
└── data/
    └── README.md         How survey responses are stored (anonymous only)
```

## 1. Research

Live interviews weren't possible, so the research combines:

1. **Student survey** (`survey/`): about 5 minutes, anonymous.
2. **Autoethnography:** my own use of Rec2Go as a regular gym-goer.
3. **One written student interview** (three questions).
4. **Heuristic walkthrough** of every Rec2Go tile, with screenshots (Nov 8, 2026).
5. **Secondary sources:** Rutgers Recreation's hours page and RURec2Go page, the App Store listing, and The Daily Targum.

### The survey

| Section | Questions |
|---|---|
| Consent | 18+ and agrees to anonymous use |
| About you | Year, visit frequency, which rec centers, activities |
| Using Rec2Go | Has the app, how they get in, what they use it for |
| Ratings (1–5 agree) | Pass is quick · easy to know what's open now · easy to find the right space · easy to find and book a class · app feels modern and trustworthy |
| Surprises | Ever shown up to find it closed, crowded or taken |
| Open questions | A time it failed them · what annoys them most · the one thing it should do before they walk in · anything else |

**Privacy:** no name, email or account, and nothing is sent to a server. At the end the participant copies a plain-text summary of their answers and sends it to the researcher. Responses are only shared publicly as anonymous summaries.

**Run it:** open `survey/index.html` in a browser, or use the GitHub Pages link above. To change questions, edit the `PAGES` list at the top of the script.

**Analysis plan:** report counts for multiple-choice answers, medians and ranges for the 1–5 ratings, and themes coded from the open answers. A small convenience sample makes the results indicative, not generalizable.

## 2. Define

- **Problem statement:** students need quick answers to "Can I get in?", "What's open?" and "Can I join that class?", and the current app is organized around departments instead of those questions.
- **Proto-personas:** Priya the routine lifter (primary), Marcus the class-goer, and Devin the pickup player. They're composites built from evidence, to be checked against survey and test results.
- **Journey map:** a weekday gym visit. The lowest points are checking hours and getting in the door.

## 3. Prototype (Figma plugin)

`figma-plugin/` builds 10 linked iPhone screens (390 × 844) as editable layers with working prototype connections.

| # | Screen | Key decision |
|---|---|---|
| 1 | Home | Profile top-left, Pass top-right; "Open now near you" card instead of a promo; today's classes |
| 2 | Member pass | Full-screen barcode, brightness boost, works offline |
| 3 | Open now | All campuses in one list, filtered by activity (basketball shown) |
| 4 | Facility detail | Spaces open now vs. later today, plus a busy-time hint |
| 5 | Classes | Date strip; past classes marked "Ended"; Book on every card |
| 6 | Class detail | When, where, spots, level; one primary action |
| 7 | Booking confirmed | Success state, reminder, pass shortcut |
| 8 | Booked (empty) | Explains what will appear and links to classes |
| 9 | Events | Promotions get their own tab instead of a banner everywhere |
| 10 | Profile | Absorbs the Social Media, Contact Us and Notifications tiles |

**Run it:**
1. In the Figma desktop app, open a Design file.
2. Plugins > Development > Import plugin from manifest, then choose `figma-plugin/manifest.json`.
3. Run Plugins > Development > Rec2Go Redesign Prototype.
4. Press Present. The flow "Rec2Go redesign v1" starts on Home.

**Data:** facility hours, open spaces and classes are Rutgers Rec's real schedule for Sunday, Nov 8, 2026, taken from Rec2Go screenshots. Event details come from Rec2Go's own banners. Spot counts, the class description and the RUID are sample values. This was a deliberate response to Part 1, where the AI tools invented hours.

## 4. Test (planned)

3–5 participants do the same three tasks on the current app and on the prototype: show the pass, find an open basketball court, book a class. Measures are success, taps, time and a 1–5 ease rating.

## Status

| Piece | Status |
|---|---|
| Part 1 AI critique | Done |
| Evidence log, insights, proto-personas, journey map | Draft done |
| Student survey | Live, collecting responses |
| Prototype v1 (10 screens) | Built |
| Hand-refined hi-fi prototype | In progress |
| Usability testing | Planned |

## Limitations

- Proto-personas come from a small set of evidence and one written interview, and still need checking against the survey and tests.
- The survey is a small convenience sample.
- Busy-time guidance paraphrases Rutgers Rec's published advice; the prototype has no live occupancy data.

## Author

**Anushka Singh**, Rutgers University. (https://anushka02singh.github.io/personal-porfolio-site/)

A student class project, not affiliated with or endorsed by Rutgers Recreation.

## License

Code: MIT. Written material and figures: CC BY 4.0.

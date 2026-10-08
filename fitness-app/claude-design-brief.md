# Claude Design Brief: Personal Health Path App (working title)

## What I need from you

Design a storyboard and screen concepts for an iPhone and Apple Watch app. Please deliver:

1. **Storyboard flows** for every flow in section 7, frame by frame.
2. **Key screens** in light and dark mode.
3. **A design system:** color tokens, type scale, spacing, corner radii, elevation and glow, and core components (buttons, cards, chips, sheets, progress strip, tab bar).
4. **City map art direction:** the six districts, how they connect, and how the city grows.
5. **A landmark medal set:** one sample medal per district, plus the special medals.
6. **Celebration concepts:** one per body system.
7. **Watch screens:** complication, today's step, and the guided session.

## 1. The product in one paragraph

This app helps anyone get healthier without starting at the gym. It shows how few obstacles there are to starting. It uses the system from *Atomic Habits*: make it obvious, attractive, easy, and satisfying; build habits on your identity; stack habits; use 2-minute versions; never miss twice. Onboarding asks the user about goals, starting point, limits, likes, obstacles, time, and daily routine. From those answers, the app builds a **personal path** from the ground up: moves → sessions → weeks → chapters → path. It suggests a name for the path, and the user can rename it. Every suggestion is backed by research, and the research is fun to read.

**First users:** the builder and his wife, through TestFlight. Later, anyone of any age, size, or experience level.

## 2. Brand feel

- **Four words:** empowering, helpful, intuitive, fun and creative.
- **Voice:** a calm coach who explains the science in a friendly way. It celebrates wins, helps with setbacks, and always finds a way to make things work.
- **Never:** macho, gym-bro, guilt-based, or shopping-like. There's no store, no currency, and no points to spend. Avoid the look of a convenience-store rewards app.
- **Taste references:** Acorns, How We Feel, Ahead, Opal, Atoms. They share soft depth and glow on calm backgrounds, a mix of playful and polished, and color used on purpose.
- **Caution:** Atoms is the official *Atomic Habits* app. Don't use atom imagery.

## 3. Big idea: Your Health City

The map is a **city that the user builds as they get healthier**. The city is divided into **districts**. Each district is a biome tied to one body system. The user's path is a route through the city. As steps get done, buildings, parks, and landmarks appear in that district. Every user's city looks different, because every plan trains different systems.

| Body system | District biome | Neighborhood landmarks (examples) | Starting color (tune freely) | Icon shape |
|---|---|---|---|---|
| Heart & endurance (heart rate, blood pressure, VO2 max) | Sunset waterfront | Boardwalk, running track, bike lane | Coral `#FF6B5A` | Heart / pulse |
| Lungs & breath | Sky hills | Rooftop gardens, kites, hilltop lookout | Sky blue `#5BC0F8` | Cloud / wave |
| Strength | Stone quarter | Stair streets, climbing wall, old stone bridge | Sunstone amber `#FFB443` | Hexagon / block |
| Flexibility & mobility | Ocean edge | Yoga deck, pier, tide pools | Mint teal `#3DD9B8` | Ripple |
| Balance & stability | Treetop park | Canopy walkways, rope bridge, treehouse | Fern green `#7BCB5B` | Leaf / triangle |
| Recovery & sleep | Night harbor | Lantern street, observatory, quiet dock | Lavender `#A99BFF` | Moon / star |

Rules:
- The map scrolls **vertically**, made for thumbs, like Duolingo.
- **Chapters are streets or blocks.** **Steps are stops** along the route. A **body check** is a plaza at the end of each chapter.
- Each district has its own scenery, lighting, and props. The whole city still reads as one place.
- Unbuilt areas show as soft outlines or fog. Seeing what's ahead creates pull.
- The city keeps growing after a path ends. A new path, a level-up, or maintenance mode adds new streets.

## 4. Visual language

- **Style:** soft 3D for the map, landmarks, and medals. Use rounded, slightly toy-like forms, soft shadows, and gentle glow.
- **Shapes:** organic curves mixed with clean geometry. Cards and buttons use rounded geometric forms. Backgrounds and the map use organic blobs and curves.
- **Color:** a mix of a sporty base and a fresh-air base.
  - Dark mode base: ink navy around `#0E1530`
  - Light mode base: chalk cream around `#F7F5EE`
  - Primary action accent: volt lime around `#D4FF3A`. Check its contrast on light mode, and use a deeper lime there if needed.
  - Support accents: sky and mint from the fresh-air palette.
  - District colors from section 3 tag body systems. Every color also comes with its icon shape, so color-blind users can tell them apart.
- **Type:** rounded sans (SF Pro Rounded) for UI and numbers. A serif with character (New York, or similar) for headlines and moments. Everything must support Dynamic Type.
- **Themes:** light and dark. Follow the system by default, with a manual override in Settings.
- **iOS fit:** use native Liquid Glass and current iOS materials for the tab bar, sheets, toolbars, and buttons. Use custom art for the map, medals, celebrations, and library cards. It should feel native but not stock Apple, and it should hold up through future iOS updates.

## 5. Motion, haptics, sound

- **Level:** lively but smooth. Buttons bounce a little, and small surprises appear. Big moments get full treatment: path reveal, chapter complete, medal earned.
- **Step done:** a haptic tap plus an animation tied to the step's body system:
  - Lungs: a breath wave
  - Heart: a pulse burst
  - Strength: blocks stacking
  - Flexibility: a stretch ripple
  - Balance: a leaf settling
  - Recovery: stars twinkling on

  Then a new building pops up on the map.
- **Every effect can be switched off on its own:** haptics, sounds, animations. Respect Reduce Motion.

## 6. Move demos and people

- **Demos are short, looping, silent animations** of a soft 3D or clean illustrated figure. Safety comes first: show joint angles and range of motion clearly. Add an "easier" and "harder" toggle on every move.
- **The figure matches the user's profile.** By default, show a range of body sizes and genders. Show older bodies, chairs, or canes only when the user's answers say that's part of their life.
- **No mascot or character cast.**

## 7. Screens and flows

### A. Onboarding: "Starting Line"
Use one question per screen, with a progress bar. Everything is skippable, and nothing is a wall of form fields.

1. Welcome: one line on the idea ("Healthier starts smaller than you think").
2. Goals: tap cards (breathe easier, more energy, stronger, move without pain, sleep better, heart health, bend easier, stamina), then **drag to rank** the top ones.
3. Starting point: friendly self-checks ("3 flights of stairs: easy / winded / not yet").
4. Optional guided baseline tests: walk test, 30-second sit-to-stand, sit-and-reach, and resting heart rate from the Watch.
5. Limits: injuries, conditions, mobility, age range. Plain words, with "prefer not to say."
6. Likes: walking, yoga, lifting, running, swimming, dancing, sports, "nothing yet."
7. Gear at home: none, mat, bands, dumbbells, other.
8. Obstacles: pick, then **rank** them (no time, no gear, embarrassed, bored, sore, tired, don't know how, other).
9. Time budget: 2 / 5 / 10 / 20 / 30+ minutes most days.
10. Your day: drag anchors (wake, coffee, commute, lunch, TV, bed) onto a timeline.
11. Health permission: explain what's read and why before the system prompt.
12. **"Building your city"** animation: districts appear based on the user's goals.
13. **Path reveal:** a city overview, chapter streets, finish line, and a suggested path name with a rename option.

### B. Daily
- **Today (home):** today's step as the hero card, its habit stack ("After coffee → 10-minute walk"), and a small progress strip. One tap opens the full dashboard.
- **Session player:** a looping demo, timer, sets, easier/harder swap, and the Watch handoff.
- **Step complete:** the system-specific celebration and the new building on the map.
- **Obstacle Buster sheet:** "What's in the way?" Pick an excuse and get a matching 2-minute action with the reason it counts.
- **Swap sheet:** do a different move that trains the same system.

### C. City and path
- **City map:** the vertical route, districts, today's stop glowing, future areas in fog.
- **Chapter intro:** the identity line ("I'm someone who walks every day") and what this chapter builds.
- **Body check flow:** test instructions, input or Watch read, result vs last time.
- **Chapter complete:** the plaza unlocks, a medal lands, and the next street opens.

### D. Progress and dashboard
- **Systems overview:** one tile per body system with a 4-week trend.
- **Metric detail:** trend chart with a plain-language headline ("Resting HR down 3 bpm since you started"). Use "linked to," never "caused by."
- **Then vs now:** body check results side by side.

### E. "Why it works" library
- Decks sorted by district.
- **Why card, three depths:**
  1. A headline sentence
  2. A 30-second illustrated explainer
  3. "Go deeper": study chips (study type, number of people) and an **evidence-strength meter**
- A card unlocks when the user does the step it explains. Make it fun to collect and easy to read, never dry.

### F. Medals: "Landmarks"
- Medals are **soft-3D landmark tokens** that match their district: a cloud crystal, a canyon stone, a lantern.
- Types: chapter complete, personal best on a body check, Comeback, milestones (100 walks), library cards collected.
- **Medal case** screen, plus a full-screen **medal earned** moment.
- No currency and nothing to buy.

### G. Life events
- **Rejoin helper** (after 3+ days away): "Welcome back. What happened?" The options are sick, busy, travel, or lost steam. Each one gets a gentle reshaped plan. No red marks and no lost progress.
- **Path finish:** a celebration plus three doors: **New path**, **Level up**, **Maintain**.
- **Weekly check-in:** three quick questions that retune the plan.

### H. Partner
- Invite your partner.
- **Share settings:** per-item toggles for what the partner sees (medals, body checks, steps done, city). Everything is off by default.
- **Partner feed:** their wins, with a cheer button.
- **Optional friendly challenge:** opt-in only.
- **Visit their city:** view only, if they've shared it.

### I. Settings
Profile, retake onboarding questions, theme (system / light / dark), haptics, sounds, animations (each separate), notifications, Health permissions, partner sharing, units.

### J. Apple Watch
- **Complication:** today's step and the progress ring in the district color.
- **Today:** step card with a "done" tap.
- **Guided session:** timer, haptic cues for reps and rest, heart rate.
- **Step complete:** a mini celebration with a haptic.

## 8. Copy samples (for tone)

- Today card: "Your 10-minute walk. Right after coffee, like always."
- Obstacle Buster: "No time? This one takes 2 minutes. That's still a vote for the person you're becoming."
- Rejoin: "Welcome back. Life happens. Here's an easier week to get rolling again."
- Body check result: "11 sit-to-stands. Last time: 7. Your legs noticed."
- Why card headline: "About 7,000 steps a day is linked to a much longer life."

## 9. Accessibility must-haves

- WCAG AA contrast in both themes, including lime on cream.
- Never use color alone. Each system has an icon shape.
- Dynamic Type everywhere, and layouts that survive the largest sizes.
- VoiceOver labels for map stops, medals, and charts.
- Reduce Motion support, and every animation can be turned off.

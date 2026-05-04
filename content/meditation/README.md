# Meditation content notes

These notes capture the quality bar for the meditation corpus and are intended
to inform the creation of future meditation playlists. They are based on a
review of the existing files in `content/meditation/final/`.

A guided meditation here is a script with timed pauses (numbers in seconds).
Each playlist is typically a series of related sessions. We care about writing
quality, insight density (insight per minute of pause + reading), structural
arc, specificity of prompts, skillful use of Stoic philosophy (vs. generic
mindfulness), and pacing.

## Paradigms — read these before writing new content

1. **`final/grief-2022.md`** — flagship for series-level architecture. Each
   session pairs a real essay-length intro with a guided meditation and a
   closing outro that lands the lesson. Primary sources (Seneca, Marcus,
   Epictetus) are load-bearing. The series builds across sessions:
   impermanence → gratitude → purpose of grief → tragedy planning → facing
   loss → view from above.
2. **`final/calm-meditations-2024.md`** — best treatment of the dichotomy of
   control. One central insight, explored from multiple angles, with breath
   and philosophy braided together (inhale acceptance, exhale relax). Cleaner
   modern prose than the 2021/2022 vintages.
3. **`final/crisis-meditations.md`** — best time-to-insight ratio. Short,
   single-purpose meditations (Anxiety Breath, Anxiety Model, Anxiety VFA,
   Anger VFA), each ~3 minutes. The model for any future in-the-moment tools.
4. **`final/joy.md`** — cleanest newer-format example (2025, with `PT/CT/CD`
   structural markers). Tight, modern prose; explicitly cultivates positive
   emotion, which the rest of the corpus underserves.
5. **`final/meaning-2022.md`** — most philosophically ambitious. Pessimistic
   nihilism → virtues → debugging → life → gratitude → urgency. The
   "Debugging" session is the rare meditation that produces a journal-worthy
   takeaway.

If you are setting the bar with two files, use `grief-2022.md` (series-level
architecture and essayistic depth) and `crisis-meditations.md` (compression
and craft in short-form).

## Strong but not flagship

- `final/vice-2022.md` — comprehensive virtue treatment; leans on templates.
- `final/courage-meditations-2024.md` — solid, well-paced; less depth than
  grief/meaning.
- `final/discipline-meditations-feb-2022.md` — strong Seneca/Epictetus framing
  on habits.
- `final/compassion-meditations-polat.md` — distinct guest-author voice;
  "rational compassion" framing is sharp.
- `final/breathing-meditations.md` — anchors techniques to specific Stoic
  exercises (Athenodorus's count).
- `final/morning-meditations-3-2024.md`, `final/evening-meditations-3-2024.md`
  — workmanlike daily drivers; useful but not exemplary.

## Do not use as paradigms

- `final/meditation-templates.md` — literal templates with `X` / `Y`
  placeholders. Useful as scaffolding only.
- `final/daily-meditations-stems-2024.md` — outlines and scaffolding, not
  finished prose.
- `final/stoa-daily-meditations-may-2021.md` — older; contains explicit
  `[Template]` sections.
- `final/powerful-stoic-quotes-2024.md`, `final/powerful-stoic-quotes-2021.md`
  — outline-heavy; less polished narrative.
- `final/copy-stoa-content-seneca-routines-ii.md` — duplicate ("Copy of").
- `final/being-more-rational.md` — useful content but reads as a numbered
  curriculum rather than a meditation series.
- `final/act-2021-acceptance.md` — fine, but the ACT-translation feels less
  native than the pure-Stoic series.
- `final/daily-meditations-maxims-2024.md` — solid; intros thinner than the
  paradigms.
- `final/stoic-approach-to-work-course.md` — applied/specialized course, not a
  paradigm template.

## Craft patterns the paradigms share

A new meditation series should aim for all seven of these.

1. **Three-act structure per session**: substantive essay intro (~150–300
   words) → guided meditation → tight outro that lands the lesson and ends
   with a quote. Skip any one and it weakens.
2. **Primary sources are load-bearing, not garnish**. A Seneca / Marcus /
   Epictetus quote is introduced, paraphrased in plain English, applied
   inside the meditation, and echoed in the outro.
3. **Concrete prompts with action verbs**: "bring to mind," "picture,"
   "rehearse," "summarize." Never "reflect on the nature of X."
4. **Athletic-rehearsal framing**: the repeated "like a musician mentally
   rehearsing" / "like an athlete drilling a play" metaphor anchors
   visualization in something familiar and effortful.
5. **Calibrated pauses**: 10–20s for transitions, 20–45s for thinking, 45–60s
   reserved for visualization/rehearsal. Anything over 60s should be earned.
6. **Close every session with summarization + apply-to-day**, before the
   breath-and-open-eyes outro. Never let the listener leave without a
   takeaway.
7. **One central insight per session**, explored from multiple angles, rather
   than three half-developed ideas crammed together.

## Series-level guidance

- Build sessions cumulatively. `grief-2022.md` is the model: each session
  introduces a new angle that depends on what came before.
- Open the series with an essay-length intro that frames the philosophical
  territory and ends with a Stoic quote. Do not start with a meditation.
- Underserved areas worth new playlists: positive emotion (only `joy.md`
  does this well), in-the-moment crisis tools (only `crisis-meditations.md`
  does this), and applied virtue in concrete domains (work, parenting,
  conflict).
- Prefer a short, focused playlist (4–6 sessions) over a long, padded one.
  Compression reads as care; padding reads as filler.

## Frontmatter and conventions

- One playlist per `.md` file under `final/`. Sessions within the playlist
  are H1 (`#`) headings; sub-parts (Intro / Meditation / Outro) are H2.
- Pause durations are bare numbers (in seconds) on their own line, e.g. `30`.
- Quote attributions reference internal IDs where available, e.g.
  `id: 1689`. Use these consistently — they are how quotes are linked into
  the app. Look up `Quote ID` and `Sentence IDs` in
  `resources/quotes/quotes.md` (the exported Stoa quote library); do not
  invent IDs. If the quote you want is not in the export, leave the ID blank
  and flag it for an editor.
- When picking quotes across a multi-session playlist, vary the opening. The
  library skews to quotes that start with "It is...", "We...", and
  "When..."; opening several sessions with the same cadence reads as
  monotone.
- Favor short quotes (under 5 sentences). Longer passages overflow the
  in-app quote card. If a longer quote is the right one, trim to the
  load-bearing sentences and use the rest inside the meditation script.
- See `../../README.md` for the repo-level frontmatter schema and slug rules.

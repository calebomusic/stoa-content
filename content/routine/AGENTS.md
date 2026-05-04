# Drafting Routines for the Stoa App

Use this guide when helping draft new routines. The goal is content that is
faithful to Stoic philosophy, accessible to a beginner, and ready to be
narrated.

## Structure

Every routine lesson has five parts, in this order:

1. **Quote**
2. **Theory**
3. **Meditation**
4. **Commitment**
5. **Action**

Use this exact section ordering and the headings `## Quote`, `## Theory`,
`## Meditation`, `## Commitment`, `## Action`. Number lessons within a routine
with `1. # Lesson Title`, matching the format used in
`final/discipline-routines.md`.

## Quote

Pick a quote from the source material when one is provided. Aim for accuracy:
match the wording of the cited translation, do not paraphrase silently.

When no quote is provided, look one up in `resources/quotes/quotes.md` — the
exported Stoa quote library, with `Quote ID` and `Sentence IDs` already
assigned. Use the `Quote ID` from that file verbatim as the `Id` in the
lesson; do not invent IDs. Only fall back to a quote that is not in the export
as a last resort, and mark it clearly so an editor can replace it.

When choosing across a multi-lesson routine, vary the opening of the quotes.
The library skews heavy on quotes that start with "It is...", "We...", and
"When..."; pulling several of those in a row reads as monotone.

Format:

```
“Never let the future disturb you. You will meet it, if you have to, with the
same weapons of reason which today arm you against the present.”
Id: 14
Source: Meditations
Location: 7.8
```

Leave `Source` or `Location` blank if unknown. The `Id` should always be
present when the quote came from `resources/quotes/quotes.md`.

## Theory

Three rules:

1. **Start with a hook.** Open with a concrete image, a question, or a sharp
   claim that puts the reader inside the problem. Avoid throat-clearing like
   "In this lesson we will discuss..."
2. **Keep the hook consistent.** The Stoic insight you introduce in the hook
   should be the same one you develop and land on. Do not drift to a different
   topic mid-section.
3. **End with delivering value.** The last few lines should give the reader
   something they can actually use today: a reframe, a question to ask
   themselves, a way to act.

Other guidance:

- The insight should be one a beginner can apply concretely. Vague exhortations
  ("be virtuous") are not enough. Show the move, not just the principle.
- Write at an 8th grade level. Short sentences. Plain words. Do not assume the
  reader knows Stoic vocabulary. If you use a term like "dichotomy of control"
  or "amor fati," explain it the first time.
- Ground the idea with a specific person, story, or example, the way the
  Boethius and Marcus Aurelius drafts do.
- Length: roughly 250 to 600 words. Long enough to develop one idea, short
  enough that nothing is filler.

## Meditation

Follow the patterns in `final/discipline-routines.md` and
`final/marcus-aurelius-routines-2026.md`.

Shape:

- **Short introduction.** One or two lines telling the listener what they are
  about to do and why.
- **Main body.** Settle in, breath work, then the contemplative exercise that
  matches the theory section. The exercise should be the theory in practice,
  not a generic breath meditation.
- **Conclusion.** Wind down, return to breath, open eyes, and often (not
  always) end with the quote from the top of the lesson.

Style:

- Simple, direct language. Second person ("you").
- Narrators charge by the word. Cut anything that is not earning its place.
- Align the meditation tightly with the theory. If the theory is about
  voluntary discomfort, the meditation should rehearse voluntary discomfort,
  not run a generic body scan.

Pause notation:

- Represent pause length with bare numbers on their own line. Seconds.
- Common pauses in existing content: `4`, `10`, `20`, `30`, `40`, `45`, `60`.
- Do not write "pause for 30 seconds" or "[pause]". Just the number.

Example:

```
Bring your attention to your breath.

30

If your mind wanders, return to the breath.

30
```

## Commitment

A single short sentence telling the listener what to commit to today. It
should follow directly from the theory and meditation. Keep it tight: the
commitment renders in the app and long text risks overflow.

Pattern: `Today, commit to <specific behavior>.`

Examples from existing content:

- "Today, commit to using the Dichotomy of Control. Divide the things you
  encounter into things up to you, and things that are not up to you."
- "Today, commit to making one small, purposeful action that gets you closer
  to a goal."
- "Today, commit to refocusing yourself when you break from a routine or habit
  you've set for yourself."

## Action

One short sentence confirming what the user did. Past tense, second person.
Mirrors the commitment.

Pattern: `You followed through and <did the committed thing>.`

Examples:

- "You followed through and identified one area where you have discipline and
  one area for improvement."
- "You committed and made a purposeful action that got you closer to a goal."
- "You followed through and refocused when you broke a routine."

Keep it short for the same overflow reason as the commitment.

## Style rules across all sections

- Do not use em dashes. Use a period, comma, colon, or "and" instead. If you
  need a pause, start a new sentence.
- Avoid unnecessary language. Every sentence should earn its place.
- Use second person.
- Contractions are fine ("you're", "don't") and match existing voice.
- Quote attributions inside the theory or meditation use the same `Id`,
  `Source`, `Location` block format as the top-of-lesson quote.

## Frontmatter

New drafts go in `content/routine/draft/<slug>.md` with this frontmatter:

```yaml
---
title: <Human-readable title>
slug: <kebab-case-slug>
type: routine
drive_id: <id or null>
drive_url: <url or null>
modified_at: <ISO 8601 timestamp>
playlist_id: null
playlist_type: null
status: draft
---
```

Move to `content/routine/final/` once approved.

## Suggested improvements to this process

These are suggestions to consider, not rules:

1. **Add a sentence ID lookup step.** Drafts often have `Sentence_ID: xxx`
   placeholders. A quick pass to fill these from `resources/quotes/quotes.md`
   (which lists `Quote ID` and `Sentence IDs` for each quote) or flag the ones
   that need a new ID would save editor time later.
2. **Standardize pause durations.** Existing routines vary from 4 to 60
   seconds with no clear rationale. A short rubric (for example: 4 to 10 for
   transitions, 20 to 30 for reflection prompts, 40 to 60 for deep
   contemplation) would make narration timing more predictable.
3. **Tighten the theory hook.** Several existing drafts open with a long
   biographical paragraph before the hook lands. A one-line opener followed
   by context reads better aloud.
4. **Cross-reference theory, meditation, commitment, and action.** Treat the
   four as one tightly linked set: the meditation rehearses the theory, the
   commitment names the behavior, the action confirms it. If any of the four
   could be swapped into a different lesson without breaking, the alignment is
   too loose.
5. **Cap meditation length.** The longer meditations in the corpus run past
   what most listeners will sit through on a phone. Aim for 4 to 7 minutes of
   spoken content per lesson unless there is a reason to go longer.
6. **Read the draft aloud before finalizing.** The narrators read this. Awkward
   phrasing, repeated words, and tongue-twisters surface immediately when
   spoken.

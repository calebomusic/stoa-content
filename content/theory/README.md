# Theory — Notes for Future Playlists & Courses

These notes are based on a review of the existing pieces in `final/`. They are meant to inform the creation of future theory playlists and courses — what to imitate, what to avoid, and which existing pieces to put in front of writers as paradigms.

## Paradigm pieces

When briefing a writer or planning a new course, point at one of these as the model.

### Tier 1 — strongest paradigms

- **`role-models-2026.md`** — Model for *biographical / narrative* content. Profiles (Cato, Marcus, Epictetus, Seneca, Socrates, Porcia, Diogenes) each open with a one-line thesis, anchor a single virtue to one or two concrete anecdotes, and close with a takeaway. Tight prose, no scaffolding.
- **`dichotomy-of-control-theory.md`** — Model for *deep-dive courses on a single concept*. Five lessons, each layering a new frame (control → cause/dependence → identity → value). Goes to the Greek (`eph' hēmin`, `prohairesis`) only where it buys the reader something. Actively dismantles common misreadings before defending the position.
- **`stoic-psychology.md`** — Model for *explaining the machinery of Stoicism*. Sustains the city / border-guards metaphor across four lessons (Impression → Reflection → Assent → Impulse). Ends with a payoff — "you've actually just mastered the dichotomy of control" — that retroactively unifies the course.
- **`anxiety-theory.md`** — Model for *problem-targeted series* (anyone struggling with X). Opens by naming the audience honestly. Pairs Stoic doctrine with modern voices (Nesse's smoke detector, Gallwey's Inner Game) in a way that feels integrated, not name-dropped.
- **`stoa-letter-goodhart-s-law.md`** — Model for *short-form (Stoa Letter)*. ~30 lines: hook with a non-Stoic idea, two everyday illustrations, pivot to Stoicism via a single primary-source quote, one action prompt. Highest insight-per-minute in the folder.

### Tier 2 — also strong, worth imitating

- **`stoicism-and-emotions-101.md`** — Carries one genuinely original teaching device (the "utility vs reflective approach" frame) and uses it to anticipate misreadings. Good model for content that has to correct misconceptions while introducing.
- **`antifragile.md`** — Model for *integrating a modern concept* (Taleb) without going pop. Hydra-vs-phoenix metaphor sustains across multiple lessons; via negativa / black swan extensions show how to keep a frame productive.
- **`theory-the-meaning-of-life.md`** — Clean eudaimonia overview. The cart metaphor is doing real work.
- **`stoic-value-theory.md`** — Rigorous philosophical scaffolding for Good / Bad / Indifferent. Use as the model when an argument is the whole point.
- **`four-virtues-theory.md`** — A single example (the boss bullying a coworker) is threaded through all four virtues. Good template for showing how virtues interlock.

## Patterns the best pieces share

Use these as a checklist when commissioning or reviewing new theory content.

- **Thesis up front.** First sentence states the claim. No warm-up.
- **One sustained metaphor per piece.** City and border guards. Hydra and phoenix. Cart and walker. The metaphor reappears across lessons and earns its keep — it isn't decorative.
- **Specific examples, not generic ones.** "The bartender at a popular club." "Booking a flight to Winnipeg thinking you're visiting Canada's capital." "The boss bullying a coworker behind their back." Vague examples ("imagine someone has wronged you") are weaker.
- **Greek terms only where they buy something.** `eph' hēmin`, `prohairesis`, `eudaimonia`, `prosoche` work because each unlocks a non-obvious meaning. Don't import Greek for flavor.
- **Anticipate the misreading.** The strongest pieces name the wrong reading of a doctrine before defending the right one (e.g. "control isn't really about control"; "Stoicism isn't unrealistic optimism").
- **Layered structure.** Multi-lesson courses build, they don't just enumerate. Each lesson should make the previous one bigger.
- **Earn the payoff.** End lessons with a concrete action, a primary-source quote that lands harder for the prior context, or a structural payoff (now you understand X).
- **Primary-source quotes do work.** The best quotes are short, in context, and immediately reframed in the writer's own voice — not block-quoted as decoration.
- **Modern bridges are welcome.** Nesse, Gallwey, Taleb, Frankl, Lisa Feldman Barrett are used integratively. The bar: the modern source must be doing something the Stoic source isn't already doing on its own.

## Anti-patterns to avoid

- **Template scaffolding leaking into final.** `CT: TBD`, `CD: TBD`, `Id: ???`, `Source:`, `Location:` should never appear in shipped content. (`misconceptions-of-stoicism.md` is the cautionary example — ship-as-template.)
- **Empty final files.** (`stoicism-and-god.md` is just frontmatter; the longer `stoicism-and-god-stoicism-and-god.md` is the real piece.)
- **Half-finished sections.** (`philosophy-as-a-way-of-life.md` is strong through Buddhism, then the Aristotelianism section drops to bullet-point stubs.)
- **`# Rejected` sections in shipped pieces.** (`productivity.md` ships with editorial leftovers at the bottom — should be cleaned before shipping or moved out of `final/`.)
- **Pragmatic-only framings of deep ideas.** "Don't cry over spilled milk because you can't fix it" is a true but shallow read of the dichotomy of control. The strongest pieces explicitly call this out and go deeper into identity / value.
- **Generic "imagine someone…" examples.** Replace with a specific role, place, or scenario. The piece will tighten by 30%.
- **Toxic-positivity-adjacent advice.** Stoicism well-written is not "feel better." It's "see clearly and act well." Anything that drifts toward the former should be flagged.

## Format conventions observed

- Long courses use `### **CT: <Title>**` for course-topic headers and a short `CD:` (course description) one-liner.
- Quotes are followed by `Id:`, `Source:`, `Location:` lines. Where these are filled in cleanly, they help; where they're left as `???`, they look unfinished.
- Frontmatter includes `drive_id`, `drive_url`, `modified_at`, `playlist_id`, `playlist_type`, `status`. Everything currently in `final/` carries `status: final`.
- File naming is inconsistent (`-theory.md` suffix sometimes, sometimes not; some files have duplicated stems like `stoicism-and-god-stoicism-and-god.md`). Worth standardizing in the next pass.

## Suggested gaps for future content

Based on what is and isn't covered well:

- **Single-concept deep dives** in the mold of `dichotomy-of-control-theory.md` for other central ideas: assent, prohairesis, oikeiōsis, the discipline of desire, the view from above, amor fati. The dichotomy course shows the depth a single concept can sustain.
- **More short-form Stoa Letters** in the mold of Goodhart's Law — a non-Stoic frame (a law, a finding, a saying) routed through Epictetus or Seneca and ending in a single action.
- **Problem-targeted series** like `anxiety-theory.md` for other top user concerns (anger, grief, comparison, motivation collapse, work meaninglessness). This format converts well because it names the user's actual problem.
- **Companion role-model profiles** beyond the seven in `role-models-2026.md` — Musonius (already partially covered), Rusticus, Helvidius Priscus, Thrasea Paetus. The format scales.

## Pieces that need cleanup before being used as references

- `misconceptions-of-stoicism.md` — currently a template; either fill in or move out of `final/`.
- `stoicism-and-god.md` — empty; deduplicate with `stoicism-and-god-stoicism-and-god.md`.
- `philosophy-as-a-way-of-life.md` — finish the Aristotelianism section.
- `productivity.md` — strip the trailing `# Rejected` block.

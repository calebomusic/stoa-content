# stoa-content

Source-of-truth corpus of Stoa app content (theory talks, routines, etc.), synced
from the [Stoa Content Drive folder][drive] and stored as Markdown so it can be
read both by humans and by the Stoa app's ingestion code.

[drive]: https://drive.google.com/drive/folders/1wVxJytVKNhg4WHqxG2fpU6cA5_kq3jcr

## Layout

Content is organized by `<type>/<status>`:

```
content/
  theory/final/<slug>.md       # Playlist with is_theory: true
  meditation/final/<slug>.md   # Playlist with is_theory: false
  routine/final/<slug>.md      # RoutinePlaylist
  routine/draft/<slug>.md      # in-progress series (currently: Boethius)
metadata/
  playlists.json               # Playlist.id <-> title map (incl. is_theory)
  routine_playlists.json       # RoutinePlaylist.id <-> title map
resources/
  podcast/<slug>.md            # Stoa Conversations podcast transcripts
```

Type resolution: when a doc's title exactly matches a row in `metadata/*.json`,
the type is derived from that record (`is_theory` for Playlist, or `routine`
for RoutinePlaylist). Otherwise the type defaults to the source Drive folder.

Slugs are kebab-case derived from the Drive doc title, with these prefixes
stripped: `Stoa Content:`, `Stoa Routines:`, `Stoa Theory:`, `MT -`, `MT:`,
`Copy of `, `V2 `. When two docs would slug to the same name, the source
folder's slug is prefixed to disambiguate.

## Frontmatter

Each `.md` file starts with YAML frontmatter:

```yaml
---
title: "Stoa Content: Amor Fati Routines"
slug: amor-fati-routines
type: routine                # theory | meditation | routine
drive_id: 1QLgCQkhfACA0imdlJMRBwCDkIDPUUZAae5yU4H1d4Cg
drive_url: https://docs.google.com/document/d/1QLg.../edit
modified_at: 2025-03-20T15:43:08Z
playlist_id: null            # set when slug matches a row in metadata/*.json
playlist_type: null          # playlist | routine_playlist | null
status: final                # final | draft
---
```

## Resources

`resources/` holds supplementary material that is not part of the core
Drive-synced corpus but is useful for grounding, search, and reference.

### `resources/podcast/`

Auto-generated transcripts of every public episode in the [Stoa Conversations
playlist][playlist] on YouTube, fetched via `yt-dlp`'s `en-orig` automatic
captions and reflowed into prose. One `.md` file per episode with frontmatter:

```yaml
---
title: "The Stoic Case for Introspection (Episode 223)"
slug: the-stoic-case-for-introspection
episode_number: 223          # omitted when title has no "(Episode NNN)" suffix
youtube_id: HkFxjmoVtr0
youtube_url: https://www.youtube.com/watch?v=HkFxjmoVtr0
upload_date: 2026-04-30
duration: 24:18
source: youtube_auto_caption
---
```

Slugs follow the same kebab-case rules as `content/`, with `(Episode NNN)`
parsed out into `episode_number`. When two distinct videos share a slug
(e.g. a re-upload), the YouTube ID is appended to disambiguate.

Because these are auto-generated captions, the prose is unedited: expect
mistranscribed names ("Caleb Monttoveros", "So Conversations") and no
punctuation reflow. Treat them as searchable references, not publishable
copy.

[playlist]: https://www.youtube.com/playlist?list=PLIQ69U4Ez45-UsP4WqlEG_1Q0rARkqbk9

## Out of scope

The following Drive items are intentionally not synced into this repo:
`Music/`, `Stoa - Assets/`, `Advertisements/`, `Archive/`, `Final/`,
`Meditations/`, `Events/` (audio/video only), the asset spreadsheets,
`intro.png`, `Stoa Content: Podcast Ad`, `Stoa Content: Routine Playlist images`,
and `Stoa Content: Models [NO IDS]`.

# Chen Reading #1

Static student-facing app for Chen W.'s 50 Korean beginner reading topics.

## Open

- Public URL: `https://g4jy.github.io/korean-practice-chen/`
- Static file: `index.html`

The app can run as a static file, but local HTTP is better for browser QA and
audio loading.

## What It Includes

- 50 topics parsed from `source_text.txt`
- 500 sentence-level Korean reading lines
- 630 vocabulary cards
- Topic 1-13 initial status from Jay's supplied known/unknown checklist
- Initial status: 163 known, 51 unknown, 416 unchecked
- 550 local Edge TTS MP3 files:
  - 50 topic-level files
  - 500 sentence-level files

## Student Flow

1. Pick a topic.
2. Check vocabulary before reading.
3. Mark each word as Known or Unknown.
4. Reveal meanings only when needed.
5. Play the whole topic or individual sentences.
6. Use `Unknown only` to review difficult words across all topics.

## Progress Storage

The shipped status in `data/app_data.js` is the first-load baseline. After a
student changes any word status, progress is saved in that student's own
browser through `localStorage` under:

- `korean-practice-chen-reading-1-progress-v1`
- `korean-practice-chen-reading-1-reveals-v1`

Future GitHub updates should keep the same URL, storage keys, and card IDs
unless a reset or migration is intentional.

## Source And QA

- App data: `data/app_data.js`
- TTS manifest: `data/tts_manifest.json`
- Audio generation report: `data/audio_generation_report.json`
- Render QA report: `qc/playwright_render_report.json`
- Screenshots:
  - `qc/desktop_topic_01.png`
  - `qc/desktop_unknown_tray.png`
  - `qc/desktop_topic_09.png`
  - `qc/mobile_topic_01.png`

No student message, package install, deletion, or paid action was performed.

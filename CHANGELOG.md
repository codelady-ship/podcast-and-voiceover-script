# Changelog

All notable changes to this project are documented here.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and the project uses [Semantic Versioning](https://semver.org/).

## [1.1.0] - 2026-11-11

Research-driven features before the Agensi listing. See the owner's research notes (open-skills research, 2026-11-11).

### Added
- **Scored hooks:** 3 options from named patterns, each scored /15 (clear, curiosity, delivered); bigger hook bank in `references/timing.md`.
- **Engine-ready TTS blocks** in `references/tts-engines.md`: ElevenLabs v3 (audio tags, no SSML breaks), Gemini (style line, single or two speakers), Azure SSML with Azerbaijani voice names; chunking rule.
- **Two-speaker dialogue format** and a **trailer** format.
- **Guest brief** built only from what the user pastes (never invented).
- **Pronunciation guide** table in the plain-speech pass.
- **Several lengths in one run** (30 s / 60 s / 3 min).
- **Title options + thumbnail text**; **chapters checked** against YouTube and Spotify rules.
- **Repurpose pack** (3 clip scripts, post, newsletter, LinkedIn post), **transcript edit list** and **publish checklist** in `references/repurpose-and-publish.md`.
- Retention beat rule for short video (a visual or text change every 3–5 s).
- `examples/leyla-45s-reel-gemini-voice.md`.
- Agensi frontmatter (`version`, `summary`, `tags`, `keywords`, `use_cases`), `scripts/build-agensi-zip.ps1`, `LISTING.md`, evals 4–6 and blind test results in `tests/`.

### Fixed (facts checked on official pages, 2026-11-11)
- ElevenLabs Free: no commercial use and attribution required ("elevenlabs.io" or "11.ai" in the title); no voice cloning on Free.
- Gemini free tier: Flash TTS models free; free-tier text may be reviewed by humans; 18+; up to 2 speakers.
- Azure F0: 0.5 million neural characters a month.
- Spotify chapter rules added (plain text, merge chapters under 30 s); loudness now cites Apple's −16 LKFS ±1 dB, true peak −1 dBFS (no Spotify target claimed).
- Instagram AI label renamed to the current "AI label" / "AI content"; YouTube disclosure only for realistic content.

### Fixed (blind evals, 2026-11-11)
- Word counts are counted, not estimated; TTS scripts are timed without the pause allowance.
- Voice-clone refusal in 1–2 lines followed by the full alternative script in the same answer.
- Short pieces never get questions only; placeholders first.
- With no engine named, three free options; Azure az-AZ voices first for Azerbaijani.
- Respelling uses the script's own letters (ş, ç); "link in bio" on screen, not a second spoken CTA.
- Free-tier terms line given in the user's language (EN/AZ/RU ready).
- SSML mapping: `/` gets no break tag, `//` = 1 s break, total break time added to the duration; every timed block has on-screen text.
- Refusal template (1–2 sentences); long pause `//` = about 1 s everywhere, added to TTS timing.

## [1.0.0] - 2026-11-10

### Added
- First release: timed scripts with word budgets, pause and stress marks, podcast/interview/short-video formats, plain-speech pass, show notes and chapters, TTS block, AI-voice disclosure, no voice cloning of real people. MIT.

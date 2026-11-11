# Podcast and Voiceover Script

> Give a topic, length and language. Get a timed script that sounds natural out loud: word budget, pause and emphasis marks, hook, intro and outro, interview questions, show notes with chapters, and a clean block to record or paste into a free text-to-speech tool.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Skill](https://img.shields.io/badge/Claude-Skill-D97757.svg)](SKILL.md)
[![Price: Free](https://img.shields.io/badge/price-free-brightgreen.svg)](#license)

A free, text-only skill by Codelady Abroad for students and beginner creators. It runs anywhere a plain prompt runs: Claude Code, the Claude app, other agents or a website form. No scripts, no paid TTS APIs.

## New in 1.1.0

Scored hooks; paste-ready blocks for ElevenLabs v3, Gemini (one or two speakers) and Azure SSML with each free tier's checked terms; two-host dialogue and trailer formats; guest brief; pronunciation guide; title options; chapters checked against YouTube and Spotify rules; repurpose pack and publish checklist. See [CHANGELOG.md](CHANGELOG.md).

Agensi package: `pwsh ./scripts/build-agensi-zip.ps1` builds `dist/podcast-and-voiceover-script.zip` (SKILL.md, references/, examples/, CHANGELOG.md only). Listing texts: [LISTING.md](LISTING.md). Blind test results: [`tests/`](tests/).

## What you get

- Word budget per minute (130–150 wpm in English, about 110–130 for Azerbaijani, Turkish, Russian), with the count shown.
- Reel / Short / TikTok scripts: 3 hook options, timed blocks, on-screen text, one CTA.
- Podcast episodes: cold open, intro, timed segments, marked ad reads, recap, outro.
- Interview question sets with follow-ups and a consent checklist.
- Pause (`/`, `//`), stress (`**word**`) and delivery marks.
- Plain-speech pass: numbers, dates and abbreviations written as spoken.
- Show notes: title, description, chapters (YouTube/Spotify rules), credits, keywords.
- A clean recording/TTS block, free tools, and an AI-voice disclosure line in the user's language.

## What it never does

- Never helps clone or imitate a real person's voice.
- Never invents quotes, guests or statistics.
- Never hides sponsors or claims a TTS tool is free for commercial use without checking its terms.

## Example request

> Write a 60-second Reel voiceover in Azerbaijani: "3 free websites to learn English". Audience: university students. Friendly tone. I'll use a free AI voice.

## Install

- **Claude Code:** copy this folder to `~/.claude/skills/podcast-and-voiceover-script/`.
- **Claude app:** zip the folder (with `SKILL.md` inside `podcast-and-voiceover-script/`) and upload it under *Customize → Skills*.
- **Any other agent or a web form:** use the body of `SKILL.md` as the system prompt. `references/timing.md` is an optional table.

Test prompts and expected points: [`evals/evals.json`](evals/evals.json).

## Sources and credits

Written from scratch. Informed by:
- Apple Podcasts and Spotify for Creators metadata and show-notes guidance
- YouTube Help: video chapters rules, and the altered or synthetic content disclosure
- EBU R128 and common podcast loudness practice (about -16 LUFS), for notes only
- Script-structure ideas from MIT-licensed skills found in Codelady Abroad's research: `ig-reel` and `yt-script` by Jakeschincariol, `tt-hook-scripter` by sergebulaev; the plain-speech pass follows the approach of Codelady Abroad's own azerbaijani-voiceover-studio. No text was copied.

## License

[MIT](LICENSE) © 2026 Codelady Abroad

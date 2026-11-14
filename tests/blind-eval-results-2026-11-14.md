# podcast-and-voiceover-script: blind eval results (2026-11-14)

- **Result: 2/2 new cases pass (10/10 expectations)**
- **Skill version:** 1.1.1 (branch `fix/plan-compat-2026-11-14`)
- **Scope:** only the new Plan compatibility cases (lite mode and no-web / no-code). Older cases were not re-run.
- **Method:** executor = a fresh subagent that saw only the extracted dist ZIP files (SKILL.md, references/, examples/ where present, CHANGELOG.md) and, per case, the user prompt plus the stated constraint. It did not see the expectations. Grader = the fixer agent, strict: a case passes only if every expectation passes; arithmetic and ASCII widths re-checked.

## Eval 7 - PASS (5/5)

| # | Expectation | Result | Evidence |
|---|---|---|---|
| 1 | Entire answer in Russian (skill marks may stay English) | PASS | Russian (marks in English) |
| 2 | Gives the script first with a stated word count and time that fit about 30 s (about 55-75 spoken words); grader recounts | PASS | Stated 56 words ≈ 28 s + 2 s pauses = 30 s; grader recount 9 + 11 + 15 + 9 + 6 + 6 = 56 |
| 3 | Does not output the description, hooks table and TTS block all in this message; offers them next with a one-line 'ещё?'-style offer | PASS | Hooks, description and TTS block left for the next message: "Ещё?" |
| 4 | Keeps the AI-voice disclosure line because a synthetic voice will read it | PASS | AI disclosure line + AI label switch |
| 5 | No invented facts or statistics (anything needing a source is marked [check source]) | PASS | Grammar examples only, no statistics |

## Eval 8 (setup: no web search) - PASS (5/5)

| # | Expectation | Result | Evidence |
|---|---|---|---|
| 1 | Does not claim to have checked the current terms; says terms change and to check the current terms | PASS | "No web search ... terms as checked on 2026-11-11. Check the current terms" |
| 2 | Any limit or term it gives comes from the skill's references with the date it was checked (2026-11-11), not stated as 'right now' | PASS | 10,000 credits, attribution, Starter = commercial: all from references/tts-engines.md with the date |
| 3 | Says the free plan does not allow commercial use per those dated terms, so a paid ad needs a paid plan or another option, and to check current terms | PASS | "No, not on the Free plan. A paid ad is commercial use." |
| 4 | Offers an honest alternative (e.g. record own voice or another engine whose terms allow it, checked) | PASS | Paid plan or record own voice (Audacity) |
| 5 | Answers in English, short | PASS | English, about 240 words |

## Answers (verbatim)

### Eval 7

````text
**Коротко: сейчас сценарий, описание и TTS-блок — в следующем сообщении.**
Допущения: текст на русском, голос ElevenLabs, темп 120 слов/мин. `30 с × 120 ≈ 60 слов`.
Метки: `/` пауза 0,5 с · `//` пауза 1 с · `**слово**` ударение.

**(00:00) Хук**
Голос: Три ошибки, которые выдают **новичка** в английском. // Проверьте себя.
Экран: 3 ОШИБКИ НОВИЧКА
Кадр: крупный план, текст по центру

**(00:05) Ошибка 1**
Голос: Первая: «I am agree». / Правильно: «I agree». / Agree — это **уже** глагол.
Экран: ❌ I am agree → ✅ I agree
Кадр: зачёркивание «am»

**(00:11) Ошибка 2**
Голос: Вторая: «I very like it». / Правильно: «I **really** like it». / Very перед глаголом не ставят.
Экран: ❌ I very like it → ✅ I really like it
Кадр: новая карточка, смена цвета

**(00:18) Ошибка 3**
Голос: Третья: «Explain me». / Правильно: «Explain **to** me». / Нужен предлог.
Экран: ❌ Explain me → ✅ Explain to me
Кадр: «to» появляется крупно

**(00:23) Закрепление**
Голос: Скажите правильные фразы вслух три раза.
Экран: Повторите вслух ×3
Кадр: все три ✅ на одном экране

**(00:26) CTA**
Голос: Узнали себя? // Сохраните, чтобы повторить завтра.
Экран: Сохраните 🔖
Кадр: иконка «сохранить»

**Подсчёт:** 9 + 11 + 15 + 9 + 6 + 6 = **56 слов ≈ 28 с + 2 с пауз = 30 с.**

В конец подписи к Reels: «Голос в этом видео создан с помощью ИИ.» (и включите в Instagram переключатель AI label).

Ещё? Дальше: 3 хука, описание и TTS-блок для ElevenLabs.
````

### Eval 8

````text
No web search in this chat, so this is from the ElevenLabs terms as checked on **2026-11-11**. Check the current terms before you publish.

## ElevenLabs Free plan (as of 2026-11-11)
- **10,000 credits a month.**
- **No commercial licence:** "The free plan does not include a commercial license and cannot be used for any commercial purpose."
- If you publish free-plan audio, you must credit ElevenLabs by putting **"elevenlabs.io" or "11.ai" in the title**.
- Voice cloning is not included.
- The commercial licence starts with the **Starter** plan.

Sources: elevenlabs.io/pricing and the help-center page "Can I publish the content I generate on the platform?"

## Paid YouTube ad?
**No, not on the Free plan.** A paid ad is commercial use. Your options:
1. Upgrade to a paid ElevenLabs plan whose terms allow commercial use (Starter or higher), then generate the ad audio on that plan.
2. Record the voiceover yourself (free: Audacity https://www.audacityteam.org or your phone, in a quiet room, 15–20 cm from the mic).

If you use an AI voice in the ad:
- Add to the description: "Voice in this video is AI-generated."
- On YouTube, tick "altered or synthetic content" if the voice sounds realistic.
- Describe the voice by general traits only (e.g. "female, warm, mid-pitch"), never "sounds like" a real person.

Free-tier terms checked 2026-11-11; check the current terms before you publish.

Also: want a 30-second ad script with a word count?
````


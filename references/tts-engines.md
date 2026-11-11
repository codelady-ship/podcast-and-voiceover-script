# TTS engines: paste-ready blocks and free-tier terms

Terms checked on the official pages on **2026-11-11**. They change: always tell the user "check the current terms before publishing". Never say a free tier allows commercial use unless the terms below say so.

## Quick choice

| Need | Engine |
|---|---|
| Free quick test, non-commercial | ElevenLabs Free (with attribution) or Gemini in Google AI Studio |
| Two voices in one dialogue | Gemini (up to 2 speakers per request) |
| Exact pause control, Azerbaijani voices, many free characters | Azure Speech (SSML) |
| Commercial post (ads, client work, monetised channel) | A paid plan whose terms allow it, or record your own voice |

## Free-tier terms (checked 2026-11-11)

- **ElevenLabs Free:** 10,000 credits a month. "The free plan does not include a commercial license and cannot be used for any commercial purpose." If you publish free-plan audio you must credit ElevenLabs by putting **"elevenlabs.io" or "11.ai" in the title**. Voice cloning is not in the Free plan. The commercial licence starts with the Starter plan. Sources: elevenlabs.io/pricing, elevenlabs.io/docs/help-center/legal/can-i-publish-the-content-i-generate-on-the-platform
- **Gemini API / Google AI Studio (free tier):** the Flash TTS models are free of charge on the free tier (the Pro TTS model is not). On the free tier Google may use inputs and outputs to improve its products and **human reviewers may read them**, so don't paste personal or confidential text. Users must be **18 or older**. Rate limits are shown inside AI Studio, not as fixed public numbers. Up to **2 speakers** per request. Sources: aistudio.google.com/docs/pricing, aistudio.google.com/docs/terms, aistudio.google.com/docs/speech-generation
- **Azure Speech (F0 free tier):** 0.5 million neural-voice characters free per month (custom and HD voices are not free). Needs an Azure account. Source: azure.microsoft.com/en-us/pricing/details/cognitive-services/speech-services/
- **Microsoft Edge "Read aloud":** for listening checks only, not for publishing.

Line to add under any TTS block, **always in the user's language**:
- EN: `Free-tier terms checked 2026-11-11; check the current terms before you publish.`
- AZ: `Pulsuz tarif şərtləri 2026-11-11 tarixində yoxlanılıb; paylaşmazdan əvvəl cari şərtləri yoxlayın.`
- RU: `Условия бесплатных тарифов проверены 2026-11-11; перед публикацией проверьте актуальные условия.`

## Chunking

Split long scripts into chunks of about **2,000–2,500 characters**, each ending at a paragraph end, numbered `Chunk 1/4`. Keep the same voice and settings for every chunk. Leave about 0.5 s of silence between chunks when joining them.

## ElevenLabs (Eleven v3)

- Pauses: v3 does **not** read SSML `<break>` tags. Use punctuation, `...` and line breaks. Older models (Multilingual v2, Flash) accept `<break time="1.0s" />` (up to 3 s).
- Delivery: v3 understands short audio tags in square brackets, e.g. `[warmly]`, `[excited]`, `[whispers]`, `[laughs]`, `[sighs]`. At most one tag every 2–3 sentences. Remove our own marks (`/`, `**`, `(00:45)`) before pasting.
- Dialogue: generate each speaker separately, or use the dialogue mode in the ElevenLabs app if the user's plan shows it.

```
[warmly] Three free sites to learn English. ...
The first one is Duolingo.
[excited] It feels like a game, and it's free.
```

## Gemini (Google AI Studio → Generate speech)

- No SSML. Put the style in one plain sentence at the top, then the text. Pauses come from punctuation, `...` and line breaks.
- Single speaker:

```
Read this in a warm, calm, friendly voice, at a relaxed pace:
Three free sites to learn English...
```

- Two speakers: choose multi-speaker mode, give each speaker a voice from the list, and keep the names exactly as in the script:

```
Read this conversation between two friendly hosts. Aysel sounds warm and calm; Murad sounds energetic.
Aysel: Did you know the first month abroad is the hardest?
Murad: For me it was the second week.
```

## Azure Speech (SSML)

Use the exact voice name from the Azure Voice Gallery. Azerbaijani neural voices: `az-AZ-BabekNeural` (male), `az-AZ-BanuNeural` (female).

```xml
<speak version="1.0" xmlns="http://www.w3.org/2001/10/synthesis" xml:lang="az-AZ">
  <voice name="az-AZ-BanuNeural">
    İngilis dilini öyrənmək üçün üç pulsuz sayt.
    <break time="1s"/>
    Birincisi, Duolinqo.
    <emphasis level="moderate">Tamamilə pulsuzdur.</emphasis>
  </voice>
</speak>
```

Mapping from our marks: `/` → no tag (a comma or full stop is enough), `//` → `<break time="1s"/>` (add the total break time to the stated duration), `**word**` → `<emphasis level="moderate">word</emphasis>`, `[slower]` → `<prosody rate="-10%">…</prosody>`.

## Never

- Never write a prompt that asks any engine to sound like, copy or clone a real person.
- Never promise a free tier is fine for ads, client work or a monetised channel.

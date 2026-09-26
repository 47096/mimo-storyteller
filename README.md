# MiMo Storyteller

**Product — multi-character TTS stories with karaoke playback.**

Write or generate a story → voices assigned to characters → listen with live text highlight. Browser only (no backend).

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-magenta.svg)](https://47096.github.io/mimo-storyteller/) · [English](README.md) | [简体中文](README-zh-CN.md) | [繁體中文](README-zh-TW.md)

![MiMo Storyteller Demo](images/mimo-storyteller-demo.png)

---

## Why this product

Audiobooks and storytime usually mean **one narrator** and a production workflow. Storyteller turns a script into **a cast**: auto-split dialogue, design voices, generate in parallel, and follow along like karaoke — so a parent, teacher, or content creator can ship a story without a studio.

## Quick start

1. Open [the live demo](https://47096.github.io/mimo-storyteller/) (or `index.html`)  
2. ⚙️ Settings → paste [MiMo](https://platform.xiaomimimo.com) API key  
3. Write a story (or ✨ generate with AI)  
4. Assign voices → **Generate** → play  

**Privacy:** API key in `localStorage` for this origin; no analytics/cookies. Keys and audio go to the MiMo API you configure.

### Platform credits (optional)

Invite **`RRJPZE`** on [platform.xiaomimimo.com](https://platform.xiaomimimo.com?ref=RRJPZE) if you want signup credit.

![MiMo Invite](images/RRJPZE.png)

## Use cases

| Use | How |
|-----|-----|
| **Kids storytime** | Script or AI story → cast voices → read along |
| **Education / language** | Dialogue practice with speaker roles |
| **Content & podcasts** | Multi-character scenes without multiple voice actors |
| **Accessibility** | Listening + visual tracking of who speaks |

## How it works

```text
Text → segment (Name： / quotes) → character cards + voice design
    → parallel TTS → karaoke playback
```

- **3-pattern segmentation** · **24 presets + voice design** · preview per character  
- **Parallel generation** · retry failures · WAV download · speed/volume  
- **i18n** (EN / 简体 / 繁體) · mobile & a11y (focus trap, ARIA, reduced motion)

## Code

| File | Role |
|------|------|
| `index.html` / `style.css` | App shell & UI |
| `app.js` | Segmentation, TTS, playback, story AI |
| `i18n.js` | Translations |
| `API.md` | MiMo API notes |
| `benchmark.html` | Extra API bench UI |

## Limits

- Segmentation: `Name：dialogue` / quoted speech (complex narration can mis-assign)  
- Output: WAV  
- Long scripts (50+ segments) take longer to generate  

## Family

- [`mimo-reader`](https://github.com/47096/mimo-reader) — browser TTS  
- [`hum`](https://github.com/47096/hum) — AI music  
- [`hanna`](https://github.com/47096/hanna) — Chrome TTS  
- [`lux-tts`](https://github.com/47096/lux-tts) / [`qwen3-tts-voice-clone`](https://github.com/47096/qwen3-tts-voice-clone) — Colab voice demos  

**License:** MIT · [datafying](https://datafying.co/)  
Community: [CONTRIBUTING](CONTRIBUTING.md) · [SECURITY](SECURITY.md) · [CODE_OF_CONDUCT](CODE_OF_CONDUCT.md)

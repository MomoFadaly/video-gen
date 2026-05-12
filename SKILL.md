# Video Generation — AI Video from Text & Images

## What It Does
Generates AI videos from text prompts or static images using fal.ai models (Kling, Veo, LTX, Wan). Smart router picks the best model by video type.

## Engine API (programmatic)
```javascript
const videoGen = require('./engine');

// Smart router
const res = await videoGen.generateBest({ prompt, type: 'hero', outputDir: './out' });
// Returns: { ok, data: { videoPath, model, duration, cost_usd }, meta: { skill, command, duration_ms } }

// Direct calls
await videoGen.generateFromText({ prompt, duration: 5, model: 'fal-ai/ltx-video', outputDir });
await videoGen.generateFromImage({ imagePath: './hero.png', motionPrompt: 'slow zoom', outputDir });
```

## Video Types
| Type | T2V Models | I2V Models |
|------|-----------|-----------|
| `hero` | Kling Pro → Kling Standard | Kling Pro I2V → Kling Standard I2V |
| `feature` | Kling Standard → Wan T2V | Kling Standard I2V → Wan I2V |
| `ambient` | LTX Video | LTX I2V → Wan I2V |
| `preview` | LTX Video | — |

## Critical Rules
1. Every function returns `{ ok, data, error, meta }` — universal result contract.
2. For best quality: generate great image first, then animate with I2V.

## Env Vars
- `FAL_KEY` — fal.ai API key (required for all video generation)

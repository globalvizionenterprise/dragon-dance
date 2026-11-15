# DRAGONDANCE — our own Seedance-class video engine

**Entity:** DRAGONDANCE (working name — Keyz renames anytime), a GLOBAL VIZION ENTERPRISE company.
**Ordered:** Keyz, 2026-11-15 — "build bytedance n make our own seedqnce."
**What it is:** our own cinematic AI video engine in the Seedance class,
built 100% on free, open-source models running on our own ComfyUI host.
Seedance itself is closed (ByteDance sells API access; no weights exist) —
DragonDance is the own-it equivalent in that class, the same way Black
Dragon Cinema Studio is our Higgsfield-class director layer. No ByteDance
code, no paid APIs, no paywalls. It is the engine under Black Dragon AI
(the studio app) and Black Dragon Cinema Studio (the director layer).

## The stack (all free / open)

| Lane | Model | Job |
|---|---|---|
| Quality T2V/I2V | Wan 2.2 14B Lightning (lightx2v) | the cinematic workhorse — proven on our engine 2026-11-05 |
| Fast T2V | Wan 2.2 TI2V 5B | drafts, previews, volume |
| Story + sound | LTX-2.5 | multi-shot stories in one prompt, native audio built in |
| References | Ingredients library (Cinema Studio) | saved characters/props/locations fed into I2V + reference workflows |
| Long form | Scenebuilder (Cinema Studio) | shots chained to 30s+ (Seedance does 30s in one pass; ours chains — stated honestly) |
| Finish | ComfyUI upscale + grade nodes | 1080p finish, film grain, the GV look |

## Seedance capability map

- Text-to-video, cinematic → Wan 2.2 14B Lightning ✔ (proven)
- Image-to-video → Wan 2.2 I2V A14B ✔ (proven 2026-11-04)
- Native audio + lip-sync → LTX-2.5 lane ✔ (sound built in; standing law: every clip has sound + lip-sync)
- Multi-shot in one prompt → LTX-2.5 ✔
- Reference image/video/audio → Ingredients → I2V/reference workflows (wiring stage)
- 30 seconds → Scenebuilder chain (stage 3)
- 1080p → upscale pass (stage 4)

## Build stages

1. **Entity + spec** — 2026-11-15 ✔
2. **Engine session:** capture the official Wan 2.2 14B T2V graph (dual-expert,
   run sheet already written: black-dragon-ai/workflows/wan22-14b-test.README.md),
   add a `dragondance` quality model id to bd-generate's comfy lane,
   point COMFY_API_URL at the live host.
3. **Long form:** Cinema Studio Scenebuilder export → DragonDance chain render.
4. **Finish:** upscale + grade pass as a saved ComfyUI workflow.

## Rules

- Free engines only. If a lane is a paywall, it does not ship (Keyz, 2026-11-15).
- Runs under Black Dragon AI's FREE BETA (until Feb 28, 2027) — no paywalls anywhere in the chain.
- Kandinsky 6.0 (MIT, synced audio) stays on the test list as a possible extra lane.

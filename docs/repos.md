# Repo notes

Checked 2026-11-24 from each GitHub page. Versions move. Re-read the upstream README before a big build.

## 1. Rea-Video

- URL: https://github.com/JuneYaooo/rea-video
- Needs: FFmpeg and Python 3.10+
- Output: a report plus VIDEO.md, a layered text file an agent can read
- Good for: "how was this made, shot by shot?"
- Not for: rendering the new film by itself
- Licence: Apache-2.0
- Ghost Code use: if the user pastes a breakdown, follow the shot list. Do not install this inside Ghost Chat.

## 2. Awesome Opus 5.5 Videos

- URL: https://github.com/yihui-dev/awesome-opus5-5-videos
- What: prompts and links. The README said 703 prompts, 418 with a live remake, updated around 2026-10-12.
- Licence: MIT for the list. Each prompt belongs to its creator.
- Ghost Code use: borrow structure (hook, motion, end card). Do not copy a creator's prompt word for word into a product.

## 3. Lemo-Opuscar

- URL: https://github.com/lemomo-ai/lemo-opuscar
- What: 99 code-made film styles. No video model. Node 20+, FFmpeg 7+, Python 3.11+.
- Code: MIT
- Style guides (STYLE.md, DIRECTOR.md, TECHNIQUE.md): CC BY-NC 4.0, plus a narrow permission to use them while making your own film.
- Do not: vendor the style library, sell it, or drop the Markdown guides into this template repo.
- Ghost Code use: name a look in your own words (see docs/looks.md).

## 4. EffectCraft

- URL: https://github.com/storytold/effectcraft
- What: Rust motion-graphics app. README said 308 effects, JSON projects, an MCP server, and its own encoders (no FFmpeg inside).
- Status on the README: alpha, first commit 2026-10-01, not ready for paid client work.
- Licence: MIT or Apache-2.0
- Ghost Code use: reference only.

## 5. PixelFX

- URL: https://github.com/patch-gg/pixelfx
- What: 244 pixel effects. Each effect is one JS file. MIT.
- Ghost Code use: for a pixel short, write a small canvas effect inspired by this. Link the repo. Do not import the whole library unless the user adds it.

## 6. ComfyUI

- URL: https://github.com/Comfy-Org/ComfyUI
- What: local node graph for diffusion models.
- Licence: GPL-3.0. Do not copy its code into this repo or a Ghost Code app.
- Ghost Code use: skip. Ghost Media already has image and video models.

## 7. Remotion

- URL: https://github.com/remotion-dev/remotion
- What: React components become video.
- Licence: not Apache. Companies need a Remotion licence. Read https://www.remotion.dev/docs/license before shipping.
- Ghost Code use: do not start here unless the user says "Remotion" and accepts the licence.

## 8. Remotion Skills

- URL: https://github.com/remotion-dev/skills
- What: agent rules for Remotion projects (`npx remotion skills add` or `npx skills add remotion-dev/skills`).
- Ghost Code use: only after Remotion is an explicit choice.

## 9. HyperFrames

- URL: https://github.com/heygen-com/hyperframes
- What: HTML, CSS, and JS become MP4. Needs Node 22+ and FFmpeg to render. Apache-2.0.
- Skills: `npx skills add heygen-com/hyperframes`
- Ghost Code use: write the same kind of timed HTML. Rendering the MP4 happens on the user's machine, not in Ghost Media.

## 10. Three.js

- URL: https://github.com/mrdoob/three.js
- Licence: MIT
- Ghost Code use: one scene, one camera, one light. Load from a CDN only if the preview can. Otherwise draw with canvas so the file still works offline.

## 11. GSAP

- URL: https://github.com/greensock/GSAP
- Ghost Code use: fine for a preview. Before a paid product, read GreenSock's current licence. CSS is the safer default.

## 12. Blender MCP

- URL: https://github.com/ahujasid/mcp-for-blender
- Old name: blender-mcp. PyPI name: mcp-for-blender.
- Needs: Blender 3+, Python 3.10+, uv, and Blender open on that computer.
- Not affiliated with the Blender Foundation.
- Ghost Code use: do not call it. Ghost Chat has no Blender.

## 13. FFmpeg

- URL: https://github.com/FFmpeg/FFmpeg
- Ghost Code use: do not shell out to it here. Tell the user the record step:

1. Open the HTML preview full screen.
2. Record 15 seconds.
3. Or, on their computer: `ffmpeg -framerate 24 -i frame-%04d.png -c:v libx264 -pix_fmt yuv420p out.mp4`

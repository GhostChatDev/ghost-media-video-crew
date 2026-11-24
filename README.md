# Ghost Media video crew

A reading list for Ghost Code. It does not contain the 13 tools.
It tells an agent which tool to read, and which one to actually build with.

Source post: https://x.com/eluchocha/status/2124914838979682338
Researched: 2026-11-24

## What this repo is

Ghost Chat cannot run Blender, Remotion, ComfyUI, or FFmpeg inside Ghost Media.
Ghost Media makes images and short clips from a prompt.
Ghost Code can build a video as a web page, then someone records or renders it.

Use this repo as project instructions. Do not paste these upstream repos into this one.

## The 13 repos

| Job | Repo | Use it for |
| --- | --- | --- |
| Breakdown | https://github.com/JuneYaooo/rea-video | Shot list and remake plan |
| Prompts | https://github.com/yihui-dev/awesome-opus5-5-videos | Example prompts. Credit the creator |
| Looks | https://github.com/lemomo-ai/lemo-opuscar | 99 style guides. Read, do not republish |
| VFX app | https://github.com/storytold/effectcraft | Desktop motion graphics. Reference only |
| Pixels | https://github.com/patch-gg/pixelfx | 244 pixel effects, MIT, safe to learn from |
| AI nodes | https://github.com/Comfy-Org/ComfyUI | Local AI graph. GPL. Do not copy code in |
| React video | https://github.com/remotion-dev/remotion | Code-to-video. Company licence |
| Remotion rules | https://github.com/remotion-dev/skills | Agent rules for Remotion |
| HTML video | https://github.com/heygen-com/hyperframes | HTML to MP4. Best fit for Ghost Code |
| 3D | https://github.com/mrdoob/three.js | Browser 3D |
| Motion | https://github.com/greensock/GSAP | Tweens. Check licence before a product |
| Blender | https://github.com/ahujasid/mcp-for-blender | Needs Blender on a machine |
| Export | https://github.com/FFmpeg/FFmpeg | Final MP4. Not available inside Ghost Media |

## Default build for Ghost Code

1. Read `AGENTS.md`.
2. Pick one look from `docs/looks.md`. Do not clone Lemo-Opuscar.
3. Build one self-contained HTML file: 1920x1080, 24 fps timing, no paid API.
4. Motion in GSAP or CSS. 3D in Three.js from a CDN, or skip 3D.
5. If the user wants a file, tell them to record the preview, or render later with HyperFrames or FFmpeg on their own computer.

## Do not

- Do not copy STYLE.md files from Lemo-Opuscar into this repo.
- Do not copy ComfyUI source into this repo.
- Do not claim a Ghost Media render used these tools. It did not.
- Do not reuse someone else's footage, music, face, or voice.

---
<img src="https://ghostchat.tech/icons/ghost-code-dev.png" width="20" height="20" alt="" align="top"> Built by [Ghost Code Dev](https://ghostchat.tech)

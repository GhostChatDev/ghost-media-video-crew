The post lists 13 tools. I checked each GitHub page and wrote a project template you can put in a public repo so Ghost Code can read it.

**What the post is.** @eluchocha says one sentence can become a short film if the agent uses this crew: break a video down, copy a look, animate it in code, then export a file. The post also points at an article by @cryptowluha, “Fable 5.2 Field Guide.”

**One honest limit for Ghost Media.** Ghost Media makes pictures and video from a prompt (Nano Banana, Grok Imagine Video Lite, Seedance 2.0 Mini). It does not clone these repos or run Remotion, Blender, or FFmpeg. Ghost Code can use this template when it builds a video as a web page or an app. You then record or render that page, or paste a prompt into Ghost Media.

| # | Repo | What it is for | Licence to watch |
|---|---|---|---|
| 1 | [JuneYaooo/rea-video](https://github.com/JuneYaooo/rea-video) | Breaks a video into shots and says how to remake it | Apache-2.0 |
| 2 | [yihui-dev/awesome-opus5-5-videos](https://github.com/yihui-dev/awesome-opus5-5-videos) | 703 prompts behind viral code videos | MIT. Prompts belong to their creators |
| 3 | [lemomo-ai/lemo-opuscar](https://github.com/lemomo-ai/lemo-opuscar) | 99 film looks, each with a style guide | Code MIT. Style guides CC BY-NC 4.0 |
| 4 | [storytold/effectcraft](https://github.com/storytold/effectcraft) | Motion graphics app, 308 effects, agent control | MIT or Apache-2.0 |
| 5 | [patch-gg/pixelfx](https://github.com/patch-gg/pixelfx) | 244 pixel effects as small code files | MIT |
| 6 | [Comfy-Org/ComfyUI](https://github.com/Comfy-Org/ComfyUI) | Node graph for local AI pictures and video | GPL-3.0 |
| 7 | [remotion-dev/remotion](https://github.com/remotion-dev/remotion) | Video written as React code | Company licence. Not free for every company use |
| 8 | [remotion-dev/skills](https://github.com/remotion-dev/skills) | Rules so an agent writes Remotion the right way | With Remotion |
| 9 | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) | Plain HTML played back as MP4 | Apache-2.0 |
| 10 | [mrdoob/three.js](https://github.com/mrdoob/three.js) | 3D in the browser | MIT |
| 11 | [greensock/GSAP](https://github.com/greensock/GSAP) | Letters and shapes that move | Check current GreenSock terms before a paid product |
| 12 | [ahujasid/mcp-for-blender](https://github.com/ahujasid/mcp-for-blender) | Lets an agent drive Blender | Needs Blender on a computer. Not Ghost Media |
| 13 | [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg) | Turns frames into the final video file | GPL / LGPL build flags matter |

**Do not copy these repos into yours.** Link them. Lemo-Opuscar’s style guides are not free to sell as a product. Remotion has a company licence. ComfyUI is GPL. Some voice tracks in Lemo demos are not free to lift out.

**What Ghost Code should actually build.** A single HTML page: Three.js or canvas for the picture, GSAP for motion, PixelFX only if you want pixels, then a screen recording or FFmpeg if you need an MP4. HyperFrames is the closest “HTML becomes MP4” path. Blender MCP and EffectCraft need a desktop app, so they are references, not something Ghost Chat runs.

Files below. Put them in a public repo (public GitHub Actions minutes stay free). In Ghost Code, open the + menu, pick that repo, and turn on GitHub before the first message.

```md README.md
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
```

```md AGENTS.md
# Agent rules for a code-made short

Read this before writing any video page.

## Goal

Turn one sentence into a short web animation Ghost Code can preview.
Default length: 15 seconds. Default size: 1920x1080. Default rate: 24 frames per second.

## Pick a path

| User asked for | Build this | Do not build |
| --- | --- | --- |
| A short film from a sentence | One HTML file | A Remotion app, unless they asked |
| Pixel game juice | Canvas plus ideas from PixelFX | The whole PixelFX repo |
| A 3D shot | Three.js in the same HTML file | Blender |
| An MP4 | HTML first, then say how to record it | FFmpeg inside Ghost Chat |
| A remake of a video they own | A shot list in Markdown, then HTML | Uploading their video to a random site |

## Hard rules

1. One complete HTML file unless they asked for a real app repo.
2. No API keys. No paid video models. No stock footage.
3. Every moving thing must be seekable in time. Use a clock, not a random loop that drifts.
4. Credit third-party ideas in a comment at the top of the file.
5. If a style guide is CC BY-NC, imitate the idea in your own words. Do not paste their STYLE.md.
6. Remotion is only for a project the user will license themselves.
7. Blender MCP is a note, not a step. Ghost Code cannot open Blender.

## Shot recipe

Write these before code:

- Logline: one sentence.
- 4 to 8 shots. Each shot has start time, end time, and what moves.
- Palette: 5 hex colors.
- Type: one font from Google Fonts or a system font.
- Sound: none, unless they will add it later. Do not embed copyrighted music.

## Timing

At 24 fps, frame = second * 24.

- 0.0s title in
- 2.0s idea
- 8.0s turn
- 13.0s end card
- 15.0s stop

Hold the last frame. Do not loop unless they asked for a loop.

## Ghost Media handoff

If they want Ghost Media to make a clip instead of code, write a prompt in `prompts/ghost-media-prompt.md` style:

- subject
- camera
- light
- motion
- length and shape
- what must not appear

Then tell them to open Ghost Media. Do not pretend the HTML file was rendered there.
```

```md docs/repos.md
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
```

```md docs/looks.md
# Looks you can ask for

These are our words, not copies of Lemo-Opuscar style files.
If you want their exact STYLE.md, read it in their repo while you make your own film.
Do not commit their Markdown here.

| Ask for this | Picture | Motion |
| --- | --- | --- |
| Neon tubes | Black field, 2 glow colors | Lines draw on, then flicker once |
| Paper cut | Red shapes, hard edges, no gradients | Pieces slide in on beats |
| Chalk | Dark green board, dusty white type | Letters write themselves |
| News caption | Lower third, one accent bar | Bar grows, then type |
| Silent film | Grain, iris, cream and black | Slight jitter, 18 fps feel |
| Blueprint | Navy, white lines, labels | Lines trace, labels fade |
| Pixel RPG | 16-color ramp, chunky pixels | 12 fps steps, then a hit freeze |
| Satellite | Dark map, thin data lines | A scan line moves down |
| Keynote | One word, lots of empty space | Word rises 24 px and settles |
| Glass product | Soft studio, one object | Slow orbit, 8 seconds |

## Prompt shape

"Make a 15-second 1920x1080 HTML film. Look: neon tubes. Story: a family coffee farm from seed to cup. No music. No photos. End on the farm name."
```

```md docs/ghost-code-checklist.md
# Checklist

- [ ] Repo is public, or you accept GitHub minute use on a private repo
- [ ] Ghost Code: + menu, pick this repository, GitHub on
- [ ] First message includes the logline, length, and look name from docs/looks.md
- [ ] Ask for one HTML file first, not 13 cloned tools
- [ ] Preview the page. Check type size on phone if the video is vertical (1080x1920)
- [ ] Record or render outside Ghost Media
- [ ] If you also want a model clip, open Ghost Media and paste a separate prompt

Time box: 45 minutes for a 15-second page. Drop 3D if the first preview is late.
```

```md prompts/example-brief.md
# Example brief

Logline: A coffee seed becomes a cup, told as neon tubes on black.

Length: 15 seconds
Size: 1920x1080
Look: neon tubes
Tools to imitate, not install: Three.js mood, GSAP timing, HyperFrames-style timed HTML

Shots:
1. 0-2s. A thin line draws a seed.
2. 2-6s. The line grows into a plant.
3. 6-10s. Steam becomes a cup outline.
4. 10-15s. Farm name, hold.

Do not use: stock video, copyrighted music, Lemo STYLE.md text, ComfyUI code.
```

**Practice idea.** Create an empty public repo, add these six files, then in Ghost Code pick that repo and send: “Read AGENTS.md. Make a 15-second neon-tubes HTML film about a family coffee farm. One file only.”

When you want the actual moving picture made inside the app, write the shot list here first, then make the clip in Ghost Media: sidebar, right under New chat, or [Open Ghost Media](/media).
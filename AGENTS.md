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

---
title: Example Game
year: 2026
cover: assets/games/example-game/sample-1.mp4
gallery: assets/games/example-game/sample-1.mp4, assets/games/example-game/sample-2.jpg, assets/games/example-game/sample-3.jpg, assets/games/example-game/sample-4.jpg, assets/games/example-game/sample-5.jpg, assets/games/example-game/sample-6.jpg, assets/games/example-game/sample-7.jpg, assets/games/example-game/sample-8.jpg, assets/games/example-game/sample-9.jpg, assets/games/example-game/sample-10.jpg, assets/games/example-game/sample-11.jpg, assets/games/example-game/sample-12.jpg
tags: Example, Template
role: Developer
---

# Example Game

Example Game is a template project page. Use it as both a Markdown feature reference and a writing guide for turning a game project into a clear portfolio case study.

The fastest workflow is:

1. Copy this file to `games/my-game-slug.md`.
2. Put your screenshots, trailer, and GIFs in `assets/games/my-game-slug/`.
3. Update the front matter at the top of the Markdown file.
4. Add a matching entry to `games.json` with the same `slug`.
5. Replace the tutorial text with the final project writeup pattern near the bottom of this file.

## Front Matter

The block at the top of this file controls the project page header, hero gallery, visible tags, and role metadata:

```md
---
title: My Game
year: 2026
cover: assets/games/my-game/trailer.mp4
gallery: assets/games/my-game/trailer.mp4, assets/games/my-game/01.jpg, assets/games/my-game/02.jpg
tags: Action, Prototype, Unity
role: Gameplay Programmer
---
```

Use comma-separated paths for `gallery`. If your first hero item is a trailer, put the same video path in both `cover` and the first `gallery` slot. The renderer removes duplicate gallery entries, and work cards skip video URLs so they can use the first still image instead.

Keep front matter simple:

- `title`: The display name for the project page.
- `year`: A year or short timeframe.
- `cover`: The first hero media item.
- `gallery`: Images and videos for the hero carousel.
- `tags`: Short comma-separated labels. Avoid commas inside a single tag.
- `role`: Your main role on the project.

This demo uses `sample-1.mp4` for the hero video and `sample-2.jpg` through `sample-12.jpg` for stills. The gameplay clip came from [Pexels - People playing computer games](https://www.pexels.com/video/people-playing-computer-games-9071400/). Extra stock reels `sample-13.mp4` through `sample-17.mp4` are body examples only and are not part of the hero gallery.

## Games JSON

Every Markdown page also needs a matching `games.json` entry so it appears in the works grid:

```json
{
  "slug": "my-game-slug",
  "title": "My Game",
  "year": "2026",
  "cover": "assets/games/my-game/01.jpg",
  "summary": "A one-sentence project summary for the card.",
  "tags": ["Action", "Prototype", "Unity"],
  "icon": "play"
}
```

The `slug` must match the Markdown filename without `.md`. For example, `games/overtime.md` uses `"slug": "overtime"`.

Use `summary` for the short card description. The Markdown front matter does not currently provide the card summary.

## Basic Text

Write short paragraphs that explain the project clearly. A good portfolio page should be easy to scan, but still specific enough to show what you actually did.

You can add **bold text**, *italic text*, `inline code`, and links like [your portfolio](https://example.com).

## Links

Use normal Markdown links for project destinations:

- [Play the build](https://example.com)
- [View the source](https://example.com)
- [Watch the trailer](https://example.com)
- [Read the devlog](https://example.com)

If a project is private or unreleased, say that directly and link only to public material.

## My Contributions

Strong contribution bullets are concrete and ownership-focused:

- Built the player movement controller, including acceleration tuning, coyote time, and input buffering.
- Designed the encounter spawning rules and implemented editor tools for wave setup.
- Integrated UI, audio cues, and save data for the prototype loop.

Avoid vague bullets like "worked on gameplay" when you can name the system, constraint, or result.

## Project Facts

A short facts section helps recruiters and collaborators understand the project quickly:

- Engine: Unity
- Language: C#
- Platform: Windows
- Team size: 4
- Duration: 8 weeks
- Status: Prototype

## Quotes

> Use blockquotes for short design goals, lessons learned, testimonials, or production notes.

## Image

Add a single image with regular Markdown image syntax:

![Example gameplay screenshot](assets/hero/side-visual.jpg)

Use descriptive alt text. It helps accessibility and makes the Markdown easier to maintain.

## Video

Embed a single clip with a `:::video` / `:::` block and one Markdown image line pointing at `.mp4`, `.webm`, or `.ogg`:

:::video
![Console controller clip (Pexels)](assets/games/example-game/sample-13.mp4)
:::

Note: the combined `portfolio.html` game route supports video blocks. If you use the standalone `game.html` file directly, make sure it also includes the video block preprocessing.

## Carousel

Use `:::carousel` for every inline carousel: image-only, video-only, or mixed. The carousel decides whether each slide is an image or video from the file extension. Supported video extensions are `.mp4`, `.webm`, and `.ogg`.

Image-only carousel:

:::carousel
![Neon joystick arcade floor](assets/games/example-game/sample-2.jpg)
![Monitor gameplay on screen](assets/games/example-game/sample-3.jpg)
![Environment blocking neon corridor](assets/games/example-game/sample-4.jpg)
![Environment palette study](assets/games/example-game/sample-5.jpg)
![Laptop playing a video game](assets/games/example-game/sample-6.jpg)
![Production still console and desk lighting](assets/games/example-game/sample-7.jpg)
![Headphones and workstation](assets/games/example-game/sample-8.jpg)
![Controller in hand playing](assets/games/example-game/sample-9.jpg)
![Level mood dark UI study](assets/games/example-game/sample-10.jpg)
![Shader and code vibe CRT terminal](assets/games/example-game/sample-11.jpg)
![Environment side panel](assets/games/example-game/sample-12.jpg)
:::

Video-only carousel:

:::carousel
![Gamers team scene (Pexels)](assets/games/example-game/sample-14.mp4)
![Keyboard gaming desks (Pexels)](assets/games/example-game/sample-15.mp4)
![Online gaming teen (Pexels)](assets/games/example-game/sample-16.mp4)
![Wireless controllers (Pexels)](assets/games/example-game/sample-17.mp4)
:::

Mixed image and video carousel:

:::carousel
![Gameplay clip opening beat](assets/games/example-game/sample-13.mp4)
![Neon joystick arcade floor](assets/games/example-game/sample-2.jpg)
![Gameplay clip team scene (Pexels)](assets/games/example-game/sample-14.mp4)
![Monitor gameplay on screen](assets/games/example-game/sample-3.jpg)
:::

## Code Blocks

Use code blocks for snippets, pseudo-code, shader notes, build commands, or technical breakdowns:

```js
function calculateScore(baseScore, comboMultiplier) {
    return baseScore * comboMultiplier;
}
```

Inline code also works, for example `playerHealth`, `deltaTime`, or `SpawnEnemy()`.

## Credits And Licensing

Add credits when a project uses third-party or team-created material:

- Team members and roles.
- Music, SFX, fonts, textures, plugins, and asset packs.
- Stock video or image sources.
- Any restrictions, such as private source code or unreleased builds.

This makes the page more professional and avoids confusion about what you personally created.

## Final Project Writeup Pattern

Copy this structure when you are ready to turn a project into a finished case study.

### Overview

Write 2-4 sentences explaining the game, genre, player fantasy, platform, and current status.

Example:

`Overtime is a first-person time-management horror prototype about surviving late shifts in a collapsing office. I built the core interaction loop in Unity over eight weeks with a four-person student team. The project focused on readable pressure, fast iteration, and a compact playable slice.`

### My Role

State your title, team size, timeframe, and what you owned.

Example:

`I worked as the gameplay programmer and technical designer. I owned player interaction, task logic, encounter triggers, UI feedback, and build integration.`

### Core Gameplay

Explain what the player does and why it is interesting. Keep this section player-facing before going technical.

- Complete timed objectives while managing limited information.
- Choose between safe routes and faster risky shortcuts.
- React to audio and UI warnings before encounters escalate.

### Key Contributions

Use this section for the strongest evidence of your work.

- Implemented the interaction system used by doors, terminals, pickups, and objective props.
- Created a data-driven task setup so designers could tune objectives without code changes.
- Built the prototype save flow, pause menu, and fail-state restart loop.

### Technical Challenges

Pick one or two real problems. Explain the constraint, your approach, and the result.

Example:

`The first objective system was hard-coded, which made iteration slow. I replaced it with ScriptableObject task definitions and a small runtime state machine, letting the team add new objective chains from the editor. This reduced setup time and made late balancing much easier.`

### Design Decisions

Mention decisions that show taste and reasoning, not just implementation.

- Used audio cues before visual threats so the player had fair warning.
- Kept interaction prompts minimal to preserve tension.
- Limited the first level to a small route network so repeated runs stayed readable.

### Tools Used

- Engine: Unity
- Language: C#
- Art: Blender, Photoshop
- Audio: FMOD or Unity Audio
- Production: Git, Trello, Miro

### Outcome

Close with the result:

- Released on itch.io.
- Completed as a vertical slice.
- Presented at a showcase.
- Improved a specific skill.
- Learned a specific production lesson.

Example:

`The prototype reached a complete 10-minute playable loop and was shown at our end-of-term showcase. The biggest takeaway was learning how much faster the team moved once gameplay data could be tuned outside code.`

### Links

- [Play the build](https://example.com)
- [Project page](https://example.com)
- [Source repository](https://example.com)

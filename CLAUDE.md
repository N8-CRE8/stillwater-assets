# Stillwater Assets — project brain

Claude reads this file automatically at the start of every session in this repo.
Keep it current: when a convention changes or a lesson is learned, update this file.

## What this repo is

Asset repository for Stillwater short-form vertical faith videos (prayers,
teachings, reframes), organized in release batches:

- `week1/` — first batch (upgraded visual style; verse wording uses the WEB
  translation — public domain).
- `batch1/` — second batch of shorts.
- `research/` — reference material and transcripts gathered for content ideas.

## Hard-won conventions

- **Watermark placement**: keep the watermark ABOVE the platform UI deadzone.
  Bottom-of-frame watermarks get covered by TikTok/Reels/Shorts UI (captions,
  buttons). Batch1 videos had to be redone for this — don't repeat it.
- **Verse wording**: use WEB (World English Bible) — public domain, no
  licensing issues.
- Filenames: `NN-slug.mp4`, numbered in intended posting order.

## Video/media analysis pipeline (proven in this environment)

To analyze a video from X/Twitter or elsewhere (works in Claude Code cloud
containers):

1. `pip install yt-dlp imageio-ffmpeg faster-whisper`
   (imageio-ffmpeg bundles an ffmpeg binary at
   `python3 -c "import imageio_ffmpeg; print(imageio_ffmpeg.get_ffmpeg_exe())"`)
2. Download: `yt-dlp -o video.mp4 "<tweet URL>"`
3. Frames for visual review: `ffmpeg -i video.mp4 -vf "fps=1/60,scale=960:-1" frames/min_%03d.jpg`
4. Transcribe: faster-whisper `base.en`, int8, vad_filter=True — a 47-min talk
   transcribes in ~15 min on container CPU.
5. X **Articles** (long-form posts) can't be fetched by yt-dlp; use
   `https://api.fxtwitter.com/<user>/status/<id>` — full article text is in
   `tweet.article.content.blocks` (Draft.js format), images in
   `tweet.article.media_entities`.

## Research on hand (`research/`)

- `hinton-ri-lecture-transcript.txt` + `hinton-ri-lecture-notes.md` — Geoffrey
  Hinton's Royal Institution lecture (digital vs biological intelligence, AI
  risk, machine understanding/consciousness). Rich source for content on AI,
  meaning, and what makes humans distinct.
- `claude-features-article.md` — catalogue of 17 Claude features (Projects,
  Memory, Scheduled Tasks, Skills, CLAUDE.md, Claude Design, prompt caching…).

## Workflow notes

- Cloud Claude Code sessions are ephemeral: anything worth keeping must be
  committed and pushed before the session ends. Deliverables from research
  sessions go in `research/`.
- To continue a cloud session locally: run `claude --teleport <session-id>`
  from inside a local checkout of this repo (CLI signed into the same
  claude.ai account). The `cse_…` id form is printed by the CLI picker.
- Potentially high-leverage next setups (from the features article):
  Scheduled Tasks in Cowork for recurring batch chores; a Skills/plugin pass
  for pptx/pdf/canvas work.

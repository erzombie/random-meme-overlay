# Random Meme Overlay
OBS browser overlay that shows a random SFW image from allowed subreddits (or a curated list).

## Live URL
https://<your-username>.github.io/random-meme-overlay/overlay.html?cat=cat&mode=reddit
- `cat` = category (cat, dog, game, …)
- `mode` = `reddit` or `list`
- optional: `subs=catmemes,MeowIRL` to override per-call

## Add/Change categories
Edit the `ALLOW` object inside `overlay.html` to set safe subreddits for each category.

## Curated list mode
Create `memes/<category>/index.txt` with one image URL per line (jpg/png/gif/webp on i.redd.it, preview.redd.it, i.imgur.com).

## OBS / Streamer.bot
- OBS: Browser source named **MEME_OVERLAY** in `[ALERTS]`.
- SB globals: `MEME_OVERLAY_BASE=https://<your-username>.github.io/random-meme-overlay`, `MEME_SCENE=[ALERTS]`, `MEME_SOURCE=MEME_OVERLAY`.
- Call action **MEME / ShowFromCategoryOnline** with `category=<name>` (mode defaults to reddit).

## Safety
- Reddit fetch filters NSFW, videos, galleries; only direct image hosts allowed.
- Your repo’s license applies to this code, **not** to images fetched from external sites.

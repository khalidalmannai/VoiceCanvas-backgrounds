# VoiceCanvas backgrounds

Backgrounds that the Voice Canvas app offers under **Samples → ＋ More**. The repository must
stay **public** (the app downloads without signing in).

## Add a background: just upload it

| Photo | Video |
|---|---|
| `photos/<category>/my-photo.jpg` | `videos/<category>/my-video.mp4` |

Open the category folder → **Add file → Upload files** → commit. That's all. Within about a
minute a robot (the "Build catalog" action, `.github/workflows/build-catalog.yml`):

* adds it to `catalog.json`, the list the app reads (never edit it by hand);
* makes the small preview in `thumbs/<category>/` if you didn't upload one;
* names it from the file name: `golden_sky.mp4` → "Golden sky";
* renames files with spaces, brackets or accents (`Desk Lamp (1).jpg` → `Desk-Lamp-1.jpg`).

You can watch it under the **Actions** tab (green tick = done).

**Pro or free:** every download is Pro. End a file name with `-free` (e.g.
`calm-lake-free.jpg`) to make it free for everyone.

**Your own preview** (optional): upload `thumbs/<category>/<same name>.jpg` (about 270×480).

## Categories (folder → name in the app)

| Folder | Shown as |
|---|---|
| `lofi-chill` | Lofi & chill |
| `cinematic-moody` | Cinematic & moody |
| `abstract-motion` | Abstract & motion |
| `nature-serene` | Nature & serene |
| `urban-lifestyle` | Urban & lifestyle |
| `spiritual-calm` | Spiritual & calm |
| `minimal-clean` | Minimal & clean |
| `occasions` | Occasions (Ramadan, Eid, holidays…) |

A new folder becomes a new category automatically (`city-nights` → "City nights"). A category
appears in the app once it has a background. Files directly in `photos/` or `videos/` (not in a
category folder) keep the category they already had.

## Good files

* **Photos:** `.jpg` / `.png` / `.webp`, portrait, about 1080×1920.
* **Videos:** `.mp4` (H.264), portrait 720×1280 or 1080×1920, a few seconds that loop smoothly,
  no sound needed, ideally under 10 MB. The GitHub upload page takes files up to 25 MB.
* Only upload images and videos you have the rights to share.

## Notes

* Renaming or moving a file makes the app see it as a new background (already-downloaded
  copies keep working).
* To change a shown name or Pro/free without renaming, edit that entry's `name` or `pro` in
  `catalog.json`; the robot keeps those edits while the file stays in place.
* GitHub may take a few minutes to show changes to the app (caching).

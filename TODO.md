# Ashashua Site TODO

## Contact / Identity
- [ ] **mailto address** — `Ashashua@theglobe.com` is a dead address. Decide whether to replace
      it with a real contact address, a modern form, or remove it entirely.

## Background Images
Original backgrounds were served from `backrounds/` (note original spelling) on Tripod.
All pages reference these in their `<body background="...">` attribute; `bgcolor` provides a
solid-color fallback for when the image is absent. Hunt Wayback Machine for each file below.
Once recovered, drop the file into `backrounds/` (or `images/backgrounds/` — both work as long
as the path in the HTML matches).

| Page | Original file | Status |
|------|--------------|--------|
| `index.html` | `backrounds/x.gif` | ❌ missing |
| `name.html` | `backrounds/x.gif` | ❌ missing (same file as index) |
| `when.html` | `backrounds/flashstars.gif` | ❌ missing |
| `location.html` | `backrounds/flashstars.gif` | ❌ missing (same file as when) |
| `creatures.html` | `backrounds/backroundblu.gif` | ❌ missing |
| `foods.html` | `backrounds/foodback.gif` | ❌ missing |
| `happytrees.html` | `backrounds/lunar_jelly.jpg` | ❌ missing |
| `places.html` | `backrounds/pearl.jpg` | ❌ missing |
| `poll.html` | `backrounds/2d.jpg` | ❌ missing |
| `portal.html` | `backrounds/multicolor.gif` | ❌ missing |
| `tools.html` | `backrounds/marble_blue.gif` | ❌ missing |
| `topten.html` | `backrounds/wback13.gif` | ❌ missing |
| `outcasts.html` | `backrounds/plasma.jpg` | ✅ recovered → `images/backgrounds/plasma.jpg` |

## MIDI / Audio Files
Each page originally played a specific MIDI (or WAV) via `<bgsound>`. These are preserved as
period-accurate HTML artifacts but none of the files exist yet. The modern music system
(autoplay `mp3/01. Secret of Mana.mp3`) plays on all pages as a stand-in.
Hunt replacements and drop into `midi/`; the `<bgsound>` tags are already wired up.

| Page | Original file | Notes |
|------|--------------|-------|
| `index.html` | `midi/mana.mid` | Mana series — title/intro feel |
| `when.html` | `midi/when.wav` | WAV, not MIDI — unique ambient clip |
| `creatures.html` | `midi/creaturemusic.mid` | Atmospheric creature theme |
| `foods.html` | `midi/food.mid` | |
| `happytrees.html` | `midi/manatitle1.mid` | Mana series |
| `location.html` | `midi/manafort.mid` | Mana series — fortress/map feel |
| `name.html` | `midi/sombansh.mid` | Secret of Mana track |
| `outcasts.html` | `midi/castle.mid` | Castle/dungeon feel |
| `places.html` | `midi/pureland.mid` | Secret of Mana — Pure Land |
| `portal.html` | `midi/pureland.mid` | Same as places |
| `corrath.html` | `midi/pureland.mid` | Same as places (assigned during build) |
| `poll.html` | `midi/somend.mid` | Secret of Mana ending theme |
| `tools.html` | `midi/sombest.mid` | Secret of Mana |
| `topten.html` | *(none — intentional)* | Page text explicitly notes no background music |

## Missing Assets

- [ ] **Creatures page original images** — Key creature images were not recovered from the
      original site. DALL-E placeholders are in use. Consider hunting Wayback Machine for:
      `images/wookiepoodle.gif`, `images/ruffle.jpg`
- [ ] **Outcasts page — Poochy Getting Fried** — `images_dalle/poochyfry.png` is pending.
      Generate a DALL-E image of Poochy getting fried by Ralphie The Raven's Rufflecrumb.
- [ ] **name.html spiral animation** — Review the FrontPage spiral entrance effect with dad
      to confirm the modern JS recreation looks faithful to the original.
- [ ] **Location page images** — Two images pending DALL-E surrogates (not yet generated):
      `images_dalle/n604.png` (galaxy map), `images_dalle/uranus.png` (planetary montage)
- [ ] **Winamp skin** (`topten.html`) — Original Ashashua Winamp skin (`ashashua_skin.zip`)
      was hosted on Tripod and is no longer available. Hunt Wayback Machine for the zip.
      `images/skin.jpg` (skin preview image) also not recovered.
      If skin is found, restore the download link in topten.html.
- [ ] **Location page video** — Original site had a video clip `moons.avi` hosted on xoom.com
      (now defunct). Consider hunting Wayback Machine for this file.

## Pages

- [ ] **Tree of Uselessness** (`tree.html`) — Original page was not recoverable.
      A placeholder is in place. Reinvent this page in the future — ideally ask dad
      what was originally on it.
- [ ] **Archives illustrations** — `archives.html` Sections VI and VII still have placeholder
      boxes. Drop `images_dalle/Galderian6.png` and `Galderian7.png` into `images_dalle/`
      when ready and swap in the image tags.

## Future Content

- [ ] **Ashashua 2.0 / new pages** — The Galderian 51 Archive (`archives.html`) is live.
      Consider what other new content belongs in this section as the 2026 expansion continues.

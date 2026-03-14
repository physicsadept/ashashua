# Ashashua Site TODO

## Contact / Identity
- [ ] **mailto address** — `Ashashua@theglobe.com` is a dead address. Decide whether to replace
      it with a real contact address, a modern form, or remove it entirely.

## Background Images
Original backgrounds were served from `backrounds/` (note original spelling) on Tripod.
All pages reference these in their `<body background="...">` attribute; `bgcolor` provides a
solid-color fallback for when the image is absent. Hunt Wayback Machine for each file below.
Once recovered, drop the file into `backrounds/` (or `images/backgrounds/`) and update the
path in the HTML `<body background="...">` attribute.

| Page | Original file | Status | Notes |
|------|--------------|--------|-------|
| `index.html` | `backrounds/x.gif` | ❌ missing | Also used by `name.html` |
| `name.html` | `backrounds/x.gif` | ❌ missing | Same file as index |
| `when.html` | `backrounds/flashstars.gif` | ❌ missing | Also used by `location.html` |
| `location.html` | `backrounds/flashstars.gif` | ❌ missing | Same file as when |
| `creatures.html` | `backrounds/backroundblu.gif` | ❌ missing | Blue-tinted tiled background |
| `foods.html` | `backrounds/foodback.gif` | ❌ missing | |
| `happytrees.html` | `backrounds/lunar_jelly.jpg` | ❌ missing | |
| `places.html` | `backrounds/pearl.jpg` | ❌ missing | |
| `poll.html` | `backrounds/2d.jpg` | ❌ missing | |
| `portal.html` | `backrounds/multicolor.gif` | ❌ missing | |
| `tools.html` | `backrounds/marble_blue.gif` | ❌ missing | |
| `topten.html` | `backrounds/wback13.gif` | ❌ missing | |
| `outcasts.html` | `backrounds/plasma.jpg` | ✅ restored → `images/backgrounds/plasma.jpg` | Body tag updated; colors intact |

## MIDI / Audio Files
Original `<bgsound>` tags are preserved as period-accurate HTML artifacts. Modern playback
uses per-page MP3 tracks via the autoplay JS system. See README for full rationale.

### MP3 Restoration Status
| Page | Original MIDI | MP3 Assigned | Status |
|------|--------------|--------------|--------|
| `index.html` | `midi/mana.mid` | `opening-title-angels-fear-.mp3` | ✅ done |
| `creatures.html` | `midi/creaturemusic.mid` | `gaia-s-navel-distant-thunder-.mp3` | ✅ done |
| `foods.html` | `midi/food.mid` | `town-color-of-the-summer-sky-.mp3` | ✅ done |
| `happytrees.html` | `midi/manatitle1.mid` | `upper-land-what-the-forest-taught-me.mp3` | ✅ done |
| `location.html` | `midi/manafort.mid` | `flammie-flight-bound-for-the-unknown.mp3` | ✅ done |
| `name.html` | `midi/sombansh.mid` | `fond-memories.mp3` | ✅ done |
| `outcasts.html` | `midi/castle.mid` | `banished-spirit-of-the-night-.mp3` | ✅ done |
| `places.html` | `midi/pureland.mid` | `lofty-mountains-where-the-wind-ends-.mp3` | ✅ done |
| `portal.html` | `midi/pureland.mid` | `pure-land-pure-night-.mp3` | ✅ done |
| `corrath.html` | `midi/pureland.mid` | `empire-town-tell-a-strange-tale-.mp3` | ✅ done |
| `poll.html` | `midi/somend.mid` | `kakkara-the-fairy-child-.mp3` | ✅ done |
| `tools.html` | `midi/sombest.mid` | `dark-lich-oracle-.mp3` | ✅ done |
| `topten.html` | *(none — intentional)* | `magnetremix.mp3` | ✅ done (Archive rainfall exemption) |
| `tree.html` | *(not recovered)* | `forest-into-the-thick-of-it-7-.mp3` | ✅ done (stopgap) |
| `archives.html` | *(new page)* | `01. Secret of Mana.mp3` | ✅ done |
| `when.html` | `midi/when.wav` | `01. Secret of Mana.mp3` | ❌ WAV not recovered; not a MIDI — unique ambient clip, source TBD; placeholder for now. The song intro is a bit ambient and vibey. |

> Source for SoM MIDIs: https://www.khinsider.com/midi/snes/secret-of-mana

## Missing Assets

- [ ] **Creatures page original images** — Key creature images were not recovered from the
      original site. DALL-E placeholders are in use. Consider hunting Wayback Machine for:
      `images/wookiepoodle.gif`, `images/ruffle.jpg`
- [ ] **`images/dragon.gif`** — Dragon gif used in the `index.html` mp3/download section
      (the "Ashashua Dream" techno remix block). Not recovered. Shows as alt text placeholder.
      Hunt Wayback Machine for this; it was part of the original homepage.
- [ ] **`images/Corinha.jpg`** — Original photo/image for the CorinHA outcast on `outcasts.html`.
      The CorinHA section was restored from Wayback source but the image was not recovered.
      Shows as alt text placeholder. Consider hunting Wayback or asking dad if the source file
      still exists somewhere.
- [ ] **`mp3/Ashashua_Dream.mp3`** — The "Ashashua Dream" techno remix linked from `index.html`
      (click the dragon gif). Created by WookieP on MTV's Music Generator for PSX around 1999.
      The original file was hosted on Tripod. Worth asking dad if he still has the source file —
      this one is probably unrecoverable from Wayback but may exist locally.
- [ ] **name.html spiral animation** — Review the FrontPage spiral entrance effect with dad
      to confirm the modern JS recreation looks faithful to the original.
- [ ] **Location page images** — Two images (not DALL-E) exist as surrogates:
      `images_new/n604.png` (galaxy map), `images_new/uranus.png` (planetary montage)
- [ ] **Winamp skin** (`topten.html`) — Original Ashashua Winamp skin (`ashashua_skin.zip`)
      was hosted on Tripod and is no longer available. Hunt Wayback Machine for the zip.
      `images/skin.jpg` (skin preview image) also not recovered.
      If skin is found, restore the download link in topten.html.
- [ ] **Location page video** — Original site had a video clip `moons.avi` hosted on xoom.com
      (now defunct). Consider hunting Wayback Machine for this file.
- [ ] **`when.html` WAV** — Original ambient audio clip (`when.wav`) was hosted on Tripod and
      not recovered. This is a WAV, not a MIDI — a bespoke clip. Likely unrecoverable;
      a thematic ambient replacement may be the only option.
- [ ] **Archives illustrations** — `archives.html` Sections VI and VII still have placeholder
      boxes. Drop `images_dalle/Galderian6.png` and `Galderian7.png` into `images_dalle/`
      when ready and swap in the image tags.

## Pages

- [ ] **Tree of Uselessness** (`tree.html`) — Original page was not recoverable.
      A placeholder is in place. Reinvent this page in the future — ideally ask dad
      what was originally on it.

## Future Content

- [ ] **Ashashua 2.0 / new pages** — The Galderian 51 Archive (`archives.html`) is live.
      Consider what other new content belongs in this section as the 2026 expansion continues.

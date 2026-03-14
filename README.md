# Ashashua

A faithful recreation of **Ashashua** — a fictional alien world originally created by my father in the late 1990s and hosted on Tripod. The original site was built in Microsoft FrontPage and last updated around 1999–2001. This repository recovers, restores, and lightly modernizes that site as a personal tribute.

---

## What Is Ashashua?

Ashashua is a fictional planet in a distant galaxy called Rantash, invented entirely by my dad. The site documents its creatures, foods, places, history, and culture — written with the earnest, unfiltered energy of the late-90s personal web. Creampops. Rufflecrumbs. The Tower of Lost Souls. A Winamp skin. It's all here.

---

## How It Was Recovered

Pages were recovered from the [Wayback Machine](https://web.archive.org/) (circa 1999–2001 snapshots). All Wayback Machine boilerplate — injected scripts, toolbar HTML, archive comments, and Tripod ad JavaScript — was stripped. URLs were converted from absolute Tripod/Wayback paths to relative links, and `.htm` extensions were normalized to `.html`.

---

## Fidelity Guide

### ✅ One-to-One with the Original
- All page text, lore, and story content is preserved exactly as written — typos, punctuation, and all. These are my dad's words.
- Original HTML structure, `<font>` tags, `<bgsound>` tags, table layouts, and inline styles are intact.
- IE5-era `revealTrans` page transition meta tags are preserved on the homepage.
- The Microsoft FrontPage `dynAnimation` spiral script on `name.html` is preserved in full.
- The hidden easter egg on `location.html` (a `.` linking to `when.html`) is preserved and the target page restored from source.
- `when.html` — a full page of `&nbsp;` spacers with a one-line punchline at the bottom — is preserved exactly, every spacer intact. The joke is the scroll.
- All recovered original images are used as-is.
- The top ten MIDI list, poll creature roster, and all internal navigation links are faithful to the original.

### 🔧 Functional Approximations
- **Background music**: Browsers no longer support `.mid` files natively or `<bgsound>`. The original tags are preserved as IE artifacts. An HTML5 autoplay script replaces them: music plays on page load if autoplay is permitted, otherwise on first user interaction. Each page has been assigned a specific Secret of Mana track (see [Music Restoration Map](#music-restoration-map) below). A `♪` toggle button is fixed to the top-right corner of every page.
- **Spiral entrance animation** (`name.html`): The original FrontPage `dynAnimation` script only ran on IE4/IE5. A modern JavaScript fallback using `requestAnimationFrame` and the same sinusoidal spiral math recreates the effect for current browsers. The original script remains in the file.
- **Creature poll** (`poll.html`): The original vantagenet.com voting service is long defunct. The poll form is preserved visually, but vote submission is now handled client-side: clicking Submit generates a random distribution of 10,000–20,000 votes, with your chosen creature always finishing in second place. Results randomize on every visit. The original "Current Results" link is kept as a relic.
- **`when.html` audio**: The original used a `.wav` file (`when.wav`) hosted on Tripod. The `<bgsound>` tag is preserved pointing at `midi/when.wav`; the file was not recovered.
- **Last updated timestamp** (`index.html`): Originally a static date. Now auto-updated on every git commit via a pre-commit hook.
- **Age display** (`index.html`): Originally hardcoded as "22." Now computed dynamically in JavaScript from the birthdate May 30, 1977.
- **Matrix loading screen** (`when.html`): Added as an easter egg on the hidden page — a canvas-based green Matrix rain animation with a terminal overlay. The original `when.html` required scrolling to find the punchline; the Matrix screen adds a second layer before that. Prompt: `> ...when?`

### 🎨 Deliberate Changes
- **Black backgrounds**: Several pages originally used light or white backgrounds with colored text that rendered poorly (e.g. yellow on white). The following pages were given `bgcolor="#000000"` as an editorial decision: `location.html`, `outcasts.html`, `topten.html`, `poll.html`.
- **DALL-E placeholder images**: Where original images could not be recovered from the Wayback Machine, AI-generated images were created as surrogates and stored in `images_dalle/`. Each DALL-E image is labeled beneath it: *"This depiction was approximated using primitive Earth-based imaging technology."* Affected pages: `creatures.html` (Bydo-X, Velshara), `foods.html`, `portal.html`, `happytrees.html`, `tools.html`, `outcasts.html` (Poochy), `corrath.html`, `archives.html` (Galderian1–5).
- **`tree.html` placeholder**: The original Tree of Uselessness page was not recoverable. A placeholder page was created at the root level in the same visual style as the homepage, with the `keedlelaobe.gif` image and a note that the page is missing. (`tree/Tree.html` was flattened to `tree.html` to match the site's flat file structure.)
- **`&nbsp;` indentation spam removed**: The original pages used long chains of `&nbsp;` for paragraph indentation. These were removed for readability. The `when.html` spacers were intentionally preserved as they are the joke.
- **Defunct external links**: Dead links to hosted files (e.g. the `moons.avi` video on xoom.com, the Winamp skin `.zip` on Tripod) have been commented out in the HTML with notes about the original URL.

### 🆕 New Content (2026 Expansion)
- **Bydo-X** and **Velshara**: Two new creatures added to `creatures.html`, written in a new narrative voice that complements but is distinct from the original 1999 lore.
- **Corrath**: New place added to `places.html`, with a dedicated `corrath.html` page — a commerce city with a waterfall running through it, Creampops on every corner, and Bydo-X on the outskirts.
- **The Galderian 51 Archive** (`archives.html`): A 7-section second-person narrative transmission log following a researcher through the forest, meeting Velshara, encountering the Bydo-X, and arriving at Corrath. Sections I–V illustrated with DALL-E imagery; VI–VII pending.

---

## Repository Structure

```
/
├── index.html              # Homepage
├── name.html               # How Ashashua Got Its Name
├── creatures.html          # Creature bestiary
├── foods.html              # Exotic foods
├── places.html             # Places directory
├── portal.html             # Dimensional Portal
├── happytrees.html         # Land of Happy Little Trees
├── tools.html              # Tower of Lost Souls
├── location.html           # Planetary Locations
├── when.html               # Easter egg (linked from location.html via hidden '.')
├── outcasts.html           # The Outcasts
├── topten.html             # Top Ten MIDIs / Musical Arts
├── poll.html               # Creature Poll
├── tree.html               # Tree of Uselessness (placeholder)
├── corrath.html            # Corrath — City of Commerce (new)
├── archives.html           # The Galderian 51 Archive (new)
├── images/                 # Recovered original images
│   └── backgrounds/        # Recovered background images
├── images_dalle/           # AI-generated placeholder images
├── images_new/             # New content images
├── midi/                   # Recovered MIDI files (reference / bgsound artifacts)
├── mp3/                    # MP3 tracks for modern browser playback
├── backrounds/             # Background tile images (mostly missing)
├── wayback/                # Original source HTML recovered from Wayback Machine (.txt)
├── TODO.md                 # Known gaps, missing assets, future plans
└── README.md               # This file
```

---

## Music Restoration Map

Original background music was specified per page via `<bgsound src="midi/...">` tags (IE-only, now inert). Each page has been given an MP3 surrogate from the *Secret of Mana* soundtrack, matched for mood and page content. MP3s were sourced by converting MIDIs obtained from [KHInsider's Secret of Mana MIDI archive](https://www.khinsider.com/midi/snes/secret-of-mana).

| Page | Original MIDI | Replacement Track | Rationale |
|------|--------------|-------------------|-----------|
| `index.html` | `mana.mid` | `opening-title-angels-fear-.mp3` | Iconic SoM intro; grand landing page energy |
| `creatures.html` | `creaturemusic.mid` | `gaia-s-navel-distant-thunder-.mp3` | Primal, subterranean, cave-creature feel |
| `foods.html` | `food.mid` | `town-color-of-the-summer-sky-.mp3` | Breezy town/market vibe matches the Creampop page |
| `happytrees.html` | `manatitle1.mid` | `upper-land-what-the-forest-taught-me.mp3` | SoM's lush forest overworld — literally trees |
| `location.html` | `manafort.mid` | `flammie-flight-bound-for-the-unknown.mp3` | Soaring flight theme fits the planetary map/galaxy page |
| `name.html` | `sombansh.mid` | `fond-memories.mp3` | Reflective/nostalgic; perfect for the planet's origin myth |
| `outcasts.html` | `castle.mid` | `banished-spirit-of-the-night-.mp3` | Exile and desolate wastelands tone |
| `places.html` | `pureland.mid` | `lofty-mountains-where-the-wind-ends-.mp3` | Surveying the landscape; directory/hub feel |
| `portal.html` | `pureland.mid` | `pure-land-pure-night-.mp3` | Ethereal and otherworldly; fits mysterious dimensional portals |
| `corrath.html` | `pureland.mid` | `empire-town-tell-a-strange-tale-.mp3` | Busy market town with an undertone of strangeness; Bydo-X on the outskirts |
| `poll.html` | `somend.mid` | `kakkara-the-fairy-child-.mp3` | Upbeat and playful; suits a creature voting poll |
| `tools.html` | `sombest.mid` | `dark-lich-oracle-.mp3` | SoM's darkest theme; fitting for GloomWing's Tower of Lost Souls |
| `topten.html` | *(none — intentional)* | `magnetremix.mp3` | Original page explicitly prohibits background music; the Archive's rainfall exemption applies |
| `tree.html` | *(not recovered)* | `forest-into-the-thick-of-it-7-.mp3` | Stopgap for the placeholder page |
| `archives.html` | *(new page)* | `opening-title-angels-fear-.mp3` | Placeholder; awaiting curator's selection |
| `when.html` | `when.wav` | *(pending — original was a WAV, not MIDI)* | Unique ambient clip; replacement source TBD |

> **Source**: [KHInsider — Secret of Mana (SNES) MIDI Archive](https://www.khinsider.com/midi/snes/secret-of-mana)

---

## TODO

See [`TODO.md`](TODO.md) for the full tracked list. Broadly:

- **Missing background images**: The `backrounds/` directory is largely absent. Most pages fall back to their `bgcolor` attribute. `outcasts.html` background (`plasma.jpg`) has been restored.
- **`when.html` WAV**: The original `when.wav` ambient clip has not been recovered.
- **DALL-E surrogates**: `archives.html` Sections VI and VII still need `Galderian6.png` and `Galderian7.png`.
- **Tree of Uselessness**: Original content unknown. Dad's input needed.
- **Winamp skin**: The original custom Ashashua Winamp skin may be recoverable from Wayback.
- **Spiral animation review**: The `name.html` spiral entrance effect should be reviewed with dad.

---

## The Spirit of the Thing

This site was made with love in 1999 by someone who built an entire alien world from scratch and put it on the internet just because he could. The goal of this restoration is to honor that — to keep the original voice, the original weirdness, and the original heart intact, while making sure it actually loads in a browser made in this century.

*— Dustin*

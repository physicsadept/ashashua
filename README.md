# Ashashua

A faithful recreation of **Ashashua** — a fictional alien world originally created by my father in the late 1990s and hosted on Tripod. The original site was built in Microsoft FrontPage and last updated around Y2k. This repository recovers, restores, and lightly modernizes that site as a personal tribute.

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
- **DALL-E placeholder images**: Where original images could not be recovered from the Wayback Machine, AI-generated images were created as surrogates and stored in `images_dalle/`. Each DALL-E image is labeled beneath it: *"This depiction was approximated using primitive Earth-based imaging technology."* Affected pages: `creatures.html` (Bydo-X, Velshara), `foods.html`, `portal.html`, `happytrees.html`, `tools.html`, `outcasts.html` (Poochy), `corrath.html`, `archives.html` (Galderian1–7).
- **`tree.html` placeholder**: The original Tree of Uselessness page was not recoverable. A placeholder page was created in the same visual style as the homepage, with a Galderian 51 Archive scholar note acknowledging the missing content.
- **`&nbsp;` indentation spam removed**: The original pages used long chains of `&nbsp;` for paragraph indentation. These were removed for readability. The `when.html` spacers were intentionally preserved as they are the joke.
- **`location.html` video link restored**: The original xoom.com-hosted `moons.avi` video link was restored using the Wayback Machine URL. The link is functional as a historical artifact.
- **Defunct external links**: Other dead links to hosted files (e.g. the Winamp skin `.zip` on Tripod) have been commented out in the HTML with notes about the original URL.

### 🆕 New Content (2026 Expansion)
- **Bydo-X** and **Velshara**: Two new creatures added to `creatures.html`, written in a new narrative voice that complements but is distinct from the original 1999 lore.
- **Corrath**: New place added to `places.html`, with a dedicated `corrath.html` page — a commerce city with a waterfall running through it, Creampops on every corner, and Bydo-X on the outskirts.
- **The Galderian 51 Archive** (`archives.html`): A 7-section second-person narrative transmission log following a researcher through the forest, meeting Velshara, encountering the Bydo-X, and arriving at Corrath. Sections I–VII illustrated with DALL-E imagery.

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
| `archives.html` | *(new page)* | `01. Secret of Mana.mp3` | PhysicsAdept's curated selection; it is the main theme extended into an epic soundtrack |
| `when.html` | `when.wav` | `01. Secret of Mana.mp3` | Original was a bespoke WAV, not MIDI; replacement is the extended main theme stop-gap |

---

## The Spirit of the Thing

This site was made with love in the 90's by someone who built an entire alien world from scratch and put it on the internet just because he could. The goal of this restoration is to honor that — to keep the original voice, the original weirdness, and the original heart intact, while making sure it actually loads in a browser made in this century.

*— Dustin; aka PhysicsAdept, an unknown scholar from Earth*

---

---

# TODO

## Contact / Identity

- [x] **`Ashashua@theglobe.com`** — Replaced with `wookiep@gmail.com` on all pages that linked to Ashashua directly (`index.html`, `topten.html`).
- [ ] **`Fox@usa.net`** — A link to "Fox" (credited as a collaborator on the moon video) remains on `index.html`. Decide: update with a current address, link to a profile somewhere, or leave as a historical artifact?
- [ ] **friends' links** — Add / update links to friends?

- [ ] **PhysicsAdept link** — Add a link to PhysicsAdept's personal website somewhere on the site. URL needed.

---

## Background Images

Most original backgrounds are missing. The `bgcolor` attribute on each page provides a solid-color fallback in the meantime.

**Two good resources for finding replacements:**

- **[Pixel Moondust Geocities Archive]( https://pixelmoondust.neocities.org/archives/archivedtiles )** — About 2,000 real archived Geocities tile backgrounds, organized by color and theme. All files are directly downloadable. This should be your first stop. Browse by color folder (Black, Blue, etc.) and click any file to preview or download it.
- **[GifCities]( https://gifcities.org/ )** — Searchable archive of animated GIFs from the Geocities era. Good for hunting specific original filenames. Type a filename or keyword into the search box.

**To install a recovered background:** save the file to the `backrounds/` folder (note the original spelling) and verify the `<body background="backrounds/filename.gif">` tag in the matching HTML file points to it.

| Page | Original file | Status | Suggested lookup |
|------|--------------|--------|-----------------|
| `index.html` / `name.html` | `backrounds/x.gif` | ❌ missing | [spaceblu.gif](https://file.garden/ZWlUCY4S7Xz2vypS/archived%20backgrounds/colours/black/spaceblu.gif) or [spacemag.gif](https://file.garden/ZWlUCY4S7Xz2vypS/archived%20backgrounds/colours/black/spacemag.gif) — dark space tile matching the navy palette |
| `when.html` / `location.html` | `backrounds/flashstars.gif` | ❌ missing | [Search GifCities for "flashstars"](https://gifcities.org/?q=flashstars) first; or try [bgbluestar.gif](https://file.garden/ZWlUCY4S7Xz2vypS/archived%20backgrounds/colours/black/bgbluestar.gif) as an alternative |
| `creatures.html` | `backrounds/backroundblu.gif` | ❌ missing | [backg101.gif](https://file.garden/ZWlUCY4S7Xz2vypS/archived%20backgrounds/colours/blue/backg101(2).gif) — blue tiled texture from Pixel Moondust Blue section |
| `foods.html` | `backrounds/foodback.gif` | ❌ missing | [bgconfetti.gif](https://file.garden/ZWlUCY4S7Xz2vypS/archived%20backgrounds/!!!%20NEW%20!!!/tiles/bgconfetti.gif) — festive, food-adjacent feel |
| `happytrees.html` | `backrounds/lunar_jelly.jpg` | ❌ missing | [bgpinkclouds.gif](https://file.garden/ZWlUCY4S7Xz2vypS/archived%20backgrounds/!!!%20NEW%20!!!/tiles/bgpinkclouds.gif) — soft, dreamy; matches the "lunar jelly" description |
| `places.html` | `backrounds/pearl.jpg` | ❌ missing | [bgsilver.jpg](https://file.garden/ZWlUCY4S7Xz2vypS/archived%20backgrounds/!!!%20NEW%20!!!/tiles/bgsilver.jpg) — iridescent/pearl-like texture |
| `poll.html` | `backrounds/2d.jpg` | ❌ missing | [008.gif](https://file.garden/ZWlUCY4S7Xz2vypS/archived%20backgrounds/colours/blue/008.gif) — simple 2-color tile from Pixel Moondust Blue section |
| `portal.html` | `backrounds/multicolor.gif` | ❌ missing | [bgmulticol.gif](https://file.garden/ZWlUCY4S7Xz2vypS/archived%20backgrounds/!!!%20NEW%20!!!/tiles/bgmulticol.gif) — strong candidate; near-exact filename match |
| `tools.html` | `backrounds/marble_blue.gif` | ❌ missing | [backg136.gif](https://file.garden/ZWlUCY4S7Xz2vypS/archived%20backgrounds/colours/blue/backg136(2).gif) or [search GifCities for "marble_blue"](https://gifcities.org/?q=marble_blue) |
| `topten.html` | `backrounds/wback13.gif` | ❌ missing | [Search GifCities for "wback13"](https://gifcities.org/?q=wback13) — from a numbered set; dark textured tile expected |
| `outcasts.html` | `backrounds/plasma.jpg` | ✅ restored | Restored to `images/backgrounds/plasma.jpg` |

---

## Music

Original `<bgsound>` tags are preserved as period-accurate HTML artifacts. Modern playback uses per-page MP3 tracks. Input welcome on whether any assigned tracks feel right — or whether you remember what the originals sounded like.

To browse replacement tracks: [KHInsider — Secret of Mana (SNES) MIDI Archive](https://www.khinsider.com/midi/snes/secret-of-mana)

| Page | Original MIDI | MP3 Assigned | Status | Input needed? |
|------|--------------|--------------|--------|---------------|
| `index.html` | `midi/mana.mid` | `opening-title-angels-fear-.mp3` | ✅ done | — |
| `creatures.html` | `midi/creaturemusic.mid` | `gaia-s-navel-distant-thunder-.mp3` | ✅ done | — |
| `foods.html` | `midi/food.mid` | `town-color-of-the-summer-sky-.mp3` | ✅ done | — |
| `happytrees.html` | `midi/manatitle1.mid` | `upper-land-what-the-forest-taught-me.mp3` | ✅ done | — |
| `location.html` | `midi/manafort.mid` | `flammie-flight-bound-for-the-unknown.mp3` | ✅ done | — |
| `name.html` | `midi/sombansh.mid` | `fond-memories.mp3` | ✅ done | — |
| `outcasts.html` | `midi/castle.mid` | `banished-spirit-of-the-night-.mp3` | ✅ done | — |
| `places.html` | `midi/pureland.mid` | `lofty-mountains-where-the-wind-ends-.mp3` | ✅ done | — |
| `portal.html` | `midi/pureland.mid` | `pure-land-pure-night-.mp3` | ✅ done | — |
| `corrath.html` | `midi/pureland.mid` | `empire-town-tell-a-strange-tale-.mp3` | ✅ done | — |
| `poll.html` | `midi/somend.mid` | `kakkara-the-fairy-child-.mp3` | ✅ done | — |
| `tools.html` | `midi/sombest.mid` | `dark-lich-oracle-.mp3` | ✅ done | — |
| `topten.html` | *(none — intentional)* | `magnetremix.mp3` | ✅ done | — |
| `tree.html` | *(not recovered)* | `forest-into-the-thick-of-it-7-.mp3` | ✅ stopgap | Review once page is rebuilt |
| `archives.html` | *(new page)* | `01. Secret of Mana.mp3` | PhysicsAdept's choice | Nice :) |
| `when.html` | `midi/when.wav` | *01. Secret of Mana.mp3* | ⚠️ placeholder | What should play here? |

---

## Missing Assets

- [ ] **`images/dragon.gif`** — Dragon gif used in the `index.html` mp3 section (the "Ashashua Dream" techno remix block). Not recovered. Currently shows placeholder text. Hunt Wayback Machine.
- [ ] **`mp3/Ashashua_Dream.mp3`** — The "Ashashua Dream" techno remix linked from `index.html` (click the dragon). Created with MTV's Music Generator for PSX circa 1999. Do you still have this file locally? If so, it can go right back in. Likely unrecoverable from Wayback.
- [ ] **`images/wookiepoodle.gif`** / **`images/ruffle.jpg`** — Original creature images for WookiePoodle and Rufflecrumb, not recovered from Wayback. DALL-E approximations currently in use on `creatures.html`.
- [ ] **`when.html` WAV** — Original ambient audio clip (`when.wav`) hosted on Tripod, not recovered. Do you remember what it sounded like? A thematic ambient replacement may be the only option.
- [ ] **Winamp skin** (`topten.html`) — Original custom Ashashua Winamp skin (`ashashua_skin.zip`) and its preview image (`images/skin.jpg`) not recovered. If found, restore the download link in `topten.html`.
- [ ] **`name.html` spiral animation** — Confirm the modern recreation of the FrontPage spiral entrance effect looks faithful to the original. The original only ran on IE4/IE5.
- [ ] **Location page images** — Two surrogate images currently in place: `images_new/n604.png` (galaxy map), `images_new/uranus.png` (planetary montage). Do these look right?

---

## Pages

- [ ] **Tree of Uselessness** (`tree.html`) — Original content not recoverable. A placeholder page is in place. Do you remember what was originally on this page? Restoring or reinventing it is a future project.

---

## Future Content

- [ ] **Ashashua 2.0 / new pages** — The Galderian 51 Archive (`archives.html`) is live. Consider what other new content belongs in the 2026 expansion.

---

---

# For Dad

Hi Dad! This section is just for you. It covers two things: how to make changes to the website using GitHub, and how to read the HTML source files well enough to update text, music, and images yourself if you want to.

You don't need to read all of this at once. Come back to it when you need it.

---

## Reference Links

**Music:**
- [KHInsider — Secret of Mana MIDI Archive](https://www.khinsider.com/midi/snes/secret-of-mana) — Browse and preview every Secret of Mana track. Click a track name to hear it. If you want to swap out a song for one of the pages, just let me know which track and which page.

**Background images:**
- [Pixel Moondust Geocities Archive]( https://pixelmoondust.neocities.org/archives/archivedtiles ) — About 2,000 real archived Geocities tile backgrounds from the late 90s, organized by color. Click any color folder, then click any file to preview or download it. This is the best single resource for finding something close to the original backgrounds.
- [GifCities]( https://gifcities.org/ ) — A searchable archive of animated GIFs from the Geocities era. Type a filename or keyword into the search bar and browse what comes up. Useful for hunting specific originals by name.

---

## GitHub Guide

### What GitHub is

GitHub is where the website's files are stored online and tracked over time. When you make a change and "push" it, the new version is saved and visible to everyone with access.

### What you need

1. A GitHub account — you already have one
2. **GitHub Desktop** — a free app that makes all of this visual, no typing required

**Download GitHub Desktop here:** https://desktop.github.com

### Setting up (one time only)

1. Download and install GitHub Desktop from https://desktop.github.com
2. Open it and click **Sign in to GitHub.com** — log in with your GitHub account
3. Go to **File → Clone Repository**
4. In the search box, type: `physicsadept/ashashua`
   - Or paste the full address: `https://github.com/physicsadept/ashashua`
5. Choose a folder on your computer where you want the files saved (Desktop or Documents is fine)
6. Click **Clone**

The website files will now download to your computer. You can open and edit them like any other file.

### The everyday workflow

Every time you sit down to make changes, follow this order:

```
1. Pull  →  2. Edit  →  3. Save  →  4. Commit  →  5. Push
```

---

**Step 1 — Pull** (get the latest version before you start)

In GitHub Desktop: click **Repository → Pull** at the top menu, or click the **Fetch origin** button. This makes sure you're working from the most up-to-date copy before you start editing. Always do this first.

> CLI equivalent: `git pull`

---

**Step 2 — Edit**

Go to the folder where you cloned the files and open the `.html` file you want to change in a text editor.

- Notepad works fine and is already on your computer
- **Notepad++** (free at https://notepad-plus-plus.org) is better — it color-codes the HTML so it's easier to read

---

**Step 3 — Save**

Save the file normally (Ctrl+S) when you're done editing.

---

**Step 4 — Commit**

Go back to GitHub Desktop. You'll see the changed file listed on the left side under **Changes**.

At the bottom left, there's a box that says *"Summary (required)"* — type a short note about what you did. Something like:
- `updated homepage text`
- `swapped background image on foods page`
- `fixed typo on creatures page`

Then click **Commit to main**.

> CLI equivalents:
> ```
> git add filename.html
> git commit -m "your message here"
> ```

---

**Step 5 — Push**

Click **Push origin** — the button at the top of GitHub Desktop. This sends your committed change up to GitHub so it's saved online.

> CLI equivalent: `git push`

---

### Navigating the repository on GitHub.com

You can also browse and read files directly on GitHub without downloading anything:

1. Go to https://github.com/physicsadept/ashashua
2. You'll see a list of all the files. Click any file name to read it.
3. To edit a file directly in the browser: click the file, then click the pencil icon (Edit) in the top right corner of the file view
4. After editing, scroll down and click **Commit changes** — add a short note about what you did, then click **Commit changes** again to confirm

Editing in the browser is fine for small text changes. For anything bigger (swapping images, adding files), using GitHub Desktop is easier.

---

## HTML Guide

You don't need to understand all of HTML to make useful changes. You just need to know where to look. Here's everything that matters.

### Basic page structure

Every page has this shape:

```html
<html>
<head>
  <!-- settings, music script, and page title go here -->
</head>
<body>
  <!-- the visible content goes here -->
</body>
</html>
```

Anything inside `<!-- ... -->` is a **comment** — it's invisible in the browser and safe to ignore.

Use **Ctrl+F** in your text editor to search for specific words on any page.

---

### How to find and change the music

Near the top of the `<body>` section of every page, there's a line like this:

```html
<audio id="bgmusic" src="mp3/fond-memories.mp3" loop></audio>
```

The part that says `src="mp3/..."` is the music file. To swap a track, change the filename between the quotes to a different file from the `mp3/` folder.

For example, to change the music on `name.html` from `fond-memories.mp3` to a different track:

```html
src="mp3/fond-memories.mp3"
```
→ change to:
```html
src="mp3/opening-title-angels-fear-.mp3"
```

The filenames of all available tracks are listed in the `mp3/` folder in the repository.

---

### How to find and change images

Images look like this:

```html
<img src="images/dragon.gif" width="130" height="100">
```

The part that says `src="images/..."` is the image file. To swap an image:

1. Put the new image file into the `images/` folder (or `backrounds/` for background tiles)
2. Change the filename in the `src="..."` part to match

For background images, look for the `<body>` tag at the top of the file — it looks like:

```html
<body background="backrounds/plasma.jpg" bgcolor="#000000">
```

The `background="..."` part points to the tile image. The `bgcolor="..."` is the solid-color fallback used when the image is missing.

---

### How to find and change text

Text on the page lives between `<p>` and `</p>` tags (paragraph):

```html
<p>This is some text on the page.</p>
```

Text may be wrapped in `<font>` tags that control color and size:

```html
<font color="#8080FF" size="4">This text is blue and larger.</font>
```

Text inside `<strong>` is **bold**. Text inside `<em>` is *italic*. These can be combined:

```html
<strong><em>This is bold and italic.</em></strong>
```

To change wording on any page: use Ctrl+F to search for the phrase, find it in the code, and edit the words between the tags. Don't change the tags themselves — just the text between them.

**The safe rule: only edit what's between `<tag>` and `</tag>`, never the tags themselves.**

---

## A Closing Note

Ashashua was yours first. This whole project exists because you built something, and it deserved to still exist. Thanks for letting it be restored, expanded, and shared. Any input you have — on accuracy, on memories, on what things should look or sound like — makes it better. Just let me know how I can help :)

*— Dustin*

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
- **Background music**: Browsers no longer support `.mid` files natively. The `<bgsound>` tags are preserved as IE artifacts, and an HTML5 `<audio>` element plays an MP3 surrogate (`mp3/01. Secret of Mana.mp3`) on modern browsers. The original `mana.mid` was not recovered; the current track is a stand-in pending dad's input.
- **Spiral entrance animation** (`name.html`): The original FrontPage `dynAnimation` script only ran on IE4/IE5. A modern JavaScript fallback using `requestAnimationFrame` and the same sinusoidal spiral math recreates the effect for current browsers. The original script remains in the file.
- **Creature poll** (`poll.html`): The original vantagenet.com voting service is long defunct. The poll form is preserved visually, but vote submission is now handled client-side: clicking Submit generates a random distribution of 10,000–20,000 votes, with your chosen creature always finishing in second place. Results randomize on every visit. The original "Current Results" link is kept as a relic.
- **`when.html` audio**: The original used a `.wav` file (`when.wav`) hosted on Tripod. The `<bgsound>` tag is preserved pointing at `midi/when.wav`; the file was not recovered.
- **Last updated timestamp** (`index.html`): Originally a static date. Now auto-updated on every git commit via a pre-commit hook.
- **Age display** (`index.html`): Originally hardcoded as "22." Now computed dynamically in JavaScript from the birthdate May 30, 1977.

### 🎨 Deliberate Changes
- **Black backgrounds**: Several pages originally used light or white backgrounds with colored text that rendered poorly (e.g. yellow on white). The following pages were given `bgcolor="#000000"` as an editorial decision: `location.html`, `outcasts.html`, `topten.html`, `poll.html`.
- **DALL-E placeholder images**: Where original images could not be recovered from the Wayback Machine, AI-generated images were created as surrogates and stored in `images_dalle/`. Each DALL-E image is labeled beneath it: *"This depiction was approximated using primitive Earth-based imaging technology."* Affected pages: `creatures.html`, `foods.html`, `portal.html`, `happytrees.html`, `tools.html`, `outcasts.html` (pending).
- **`tree/Tree.html` placeholder**: The original Tree of Uselessness page was not recoverable. A placeholder page was created in the same visual style as the homepage, with the `keedlelaobe.gif` image and a note that the page is missing.
- **`&nbsp;` indentation spam removed**: The original pages used long chains of `&nbsp;` for paragraph indentation. These were removed for readability. The `when.html` spacers were intentionally preserved as they are the joke.
- **Defunct external links**: Dead links to hosted files (e.g. the `moons.avi` video on xoom.com, the Winamp skin `.zip` on Tripod) have been commented out in the HTML with notes about the original URL.

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
├── when.html               # Easter egg (linked from location.html)
├── outcasts.html           # The Outcasts
├── topten.html             # Top Ten MIDIs / Musical Arts
├── poll.html               # Creature Poll
├── tree/
│   └── Tree.html           # Tree of Uselessness (placeholder)
├── images/                 # Recovered original images
├── images_dalle/           # AI-generated placeholder images
├── midi/                   # Recovered MIDI files (partial)
├── mp3/                    # MP3 surrogate tracks for modern browsers
├── backrounds/             # Background tile images (mostly missing)
├── TODO.md                 # Known gaps, missing assets, future plans
└── README.md               # This file
```

---

## TODO

See [`TODO.md`](TODO.md) for the full tracked list. Broadly:

- **Missing MIDIs**: Most background music files were not recovered. Hunting them via Wayback or sourcing period-accurate replacements is an ongoing project.
- **Missing background images**: The `backrounds/` directory is largely absent. Most pages fall back to their `bgcolor` attribute.
- **DALL-E surrogates**: Several pages still need placeholder images generated (`location.html`, `outcasts.html`).
- **Winamp skin**: The original custom Ashashua Winamp skin may be recoverable from Wayback.
- **Spiral animation review**: The `name.html` spiral entrance effect should be reviewed with dad to confirm the recreation feels right.
- **Tree of Uselessness**: The original content is unknown. Dad's input needed.
- **Ashashua 2.0**: A placeholder has been added to the homepage nav for new content coming in 2026.

---

## The Spirit of the Thing

This site was made with love in 1999 by someone who built an entire alien world from scratch and put it on the internet just because he could. The goal of this restoration is to honor that — to keep the original voice, the original weirdness, and the original heart intact, while making sure it actually loads in a browser made in this century.

*— Dustin*

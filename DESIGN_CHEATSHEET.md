# MFIMDb Design Bible
Version 2 — consolidated 24 November 2026

## APPROVED VISUAL REFERENCE (24 November 2026)
The approved mock-up from this conversation is the **orange page with pale-blue, hand-drawn cartoon scroll/ribbon banners** reading “Inside MFIMDb”, “EPISODES”, “CHARACTERS”, “THEME PARK”, “THE MUSEUM”, “THE DATABASE”, “THE LORE” and a small “the MAUDE CAST” ribbon at the bottom. This is the reference for the **shape and lettering**, not a mandate to add unbuilt navigation destinations.

**Important:** The previous CSS-only ribbons on `inside.html` were considered *janky*. Do NOT use the earlier polygon/clip-path triangular tabs or lopsided rounded rectangle as the reference. The newer approved image has coherent curled ribbon ends, smoothly curved edges and convincing black outlines.

## Visual language
- **Background:** flat, rich burnt Maudecast orange, approximately `#c84600` (match original Maudecast artwork when available); avoid gradients, purple, corporate UI styling.
- **Banners:** pale cyan/light blue approximately `#addcde`; thick, confident, slightly imperfect **black cartoon outlines**, rounded folds and visibly curled end-tails. Organic and playful but **clean, aligned and intentional**.
- **Typography:** large, black, rounded, hand-lettered, uneven cartoon lettering like the Maudecast logo. Do not substitute formal serif or ordinary UI sans-serif headings. Maintain readability.
- **Body copy:** simple, high-contrast lettering, with sufficient spacing; can be white where it reads clearly on orange.
- **Layout:** SMALL ribbons floating in a LARGE FIELD OF ORANGE. Keep the orange negative space visually dominant, like the original Maudecast Episode 1 title-card screenshot. Desktop guideline: title ribbon at most ~760px wide, menu ribbons ~280px wide, three columns with generous horizontal and vertical gaps, and small bottom ribbon ~310px. Responsive on mobile; no clipping, overlaps or text overflow.
- **Authenticity:** should feel like it came from the original hand-drawn Maudecast opening art. Reference: the small pale-blue `the MAUDE CAST` ribbon in the original video image.
- **Do not** replace working website links with a static screenshot. Recreate the approved ribbon look with reusable SVG or equivalent scalable assets, with actual accessible HTML links and live text.

## Separate palette: Episode pages (approved 24 November 2026)
These colours apply to episode detail pages such as `episode-001.html`, NOT the orange `inside.html` menu:
- **Background:** Deep purple `#160f23`
- **Text:** Warm cream `#f7e6bf`
- **Links:** Golden yellow `#ffc451`
- **Episode cards/panels:** Darker purple with bright orange borders (current episode page uses `#251a33` panels and `#f47c24` accents).
- Preserve the embedded YouTube video, episode metadata, transcript and working navigation. The episode-page palette is deliberately distinct from the orange Maudecast interior.

## Implementation / QA
1. Inspect the existing GitHub page and approved artwork before changing it.
2. Use one reusable ribbon component/asset with controlled variations in width. Curl/fold geometry must remain attached and symmetric enough to look intentional.
3. Test desktop and narrow mobile widths; verify text remains inside ribbon and links remain clickable.
4. Preserve existing content, links, Museum entrance, wig-to-home navigation and episode archive.
5. Keep artwork and navigation separate: decorative visuals must not obscure interaction targets.
6. When asked to update the design, compare against the **approved ribbon mock-up**, not the earlier CSS version.
7. Do not claim a mock-up is live until the relevant GitHub commit is made and checked.

## Current site
Repository: `boleary1599-wq/themaudecastextendeduniverse`
Homepage: `index.html` (orange chair/hair opening)
Museum: `museum.html` (wig hotspot back to home, doors into `inside.html`)
Interior: `inside.html`
Episode 1: `episode-001.html`

## Publishing workflow
Connected GitHub can update text/HTML directly. For image assets, the earlier successful workflow used Google Drive as an intermediate step, GitHub blob/tree/commit, then GitHub Pages deployment. Keep the user's manual steps at zero when possible.

**Design status:** The approved ribbon direction is implemented as functional SVG/HTML navigation in `inside.html`. The ribbon scale was reduced on 24 November 2026 to leave generous orange negative space. Keep reviewing the live rendering against the approved visual reference.


## Locked episode master — episode-001.html
Use the approved reference implementation for every episode. Required order: header and title; metadata (episode number, duration, participants); concise introduction; embedded original YouTube video; six responsive clickable navigation boxes; six corresponding panels; return navigation.
1. Museum Story (#story-so-far)
2. Spectral Speculations (#maude-story)
3. Literary Essay (#literary-essay)
4. Mauditorium (#mauditorium)
5. Sponsor (#sponsor)
6. Full Transcript (#episode-transcript)

No redundant Watch on YouTube box; the embed is the viewing control. Preserve source links. Keep the Museum and Spectral panels independent with orange and gold borders respectively. Main column 920px; deep purple #160f23, cream #f7e6bf, gold links #ffc451, orange #f47c24 header/video/nav borders; dark purple panels; Georgia essay typography. Navigation boxes: dark purple fill, orange border, gold text, visible hover and keyboard focus, wrapping on narrow screens. Include accessible skip link, focus states and reduced-motion support. No clipping or overflow.
Transcript UI: one named heading per merged speaker turn, timed cue links seek embedded video, compact cue toggle, turn/cue count, TXT and JSON downloads, provisional notice and load-error fallback. Follow Editorial Bible for transcript content and attribution. Follow Continuity Bible for narrative evidence. Do not mark a page complete if any mandatory functionality is missing.

## Episode 2 status
episode-002.html is committed as an incomplete draft. Original video ID l0xsddmsFeg has been supplied; player verification and speaker-labelled transcript are pending; do not use it as a master template.

## Narrative density and compact continuity reference
Museum Story and Spectral Speculations should read like book chapters: combine closely related short paragraphs into substantial coherent passages, normally around 70–140 words where the material supports it. Keep thematic headings and natural breaks; do not pad or omit facts. The narrative remains at normal reading size. Character and continuity ledger entries use compact approximately 12.5–13px text, tight padding and two columns on desktop, one on narrow screens. Ledger headings are subordinate to narrative headings. Preserve readability and all existing evidence. Apply to Episode 1 master and all later episodes; literary essay typography remains unchanged.

## Cumulative recap versus current episode
In each of Museum Story and Spectral Speculations, separate The Story So Far (prior episodes only, maximum approximately 300 words per universe) from This Episode (unrestricted length; exhaustive current developments and micro-details). Episode 1 needs no prior recap. Keep the compact cumulative continuity ledger separately, without a word cap. Never sacrifice current episode evidence to meet the recap limit.

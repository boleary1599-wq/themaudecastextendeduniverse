# MFIMDb — Maudecast Design Cheat Sheet

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

## MFIMDb — Mandatory Transcript Rules

**ALWAYS attribute every line of dialogue to a named speaker. NO EXCEPTIONS.**

1. **100% speaker attribution:** Every speaking turn must have a name. Never use "Unknown", "Unidentified" or blank labels.
2. **Guess when necessary:** Use the audio, context and conversational flow to identify speakers. If uncertain, make your best educated guess and flag it internally for later correction.
3. **Readable dialogue:** Format transcripts as conversations, with the speaker's name clearly displayed. Merge consecutive lines from the same speaker.
4. **Clickable timestamps:** Every speaking turn should have a timestamp linking to that moment in the embedded YouTube video.
5. **Correct Whisper errors:** Fix obvious transcription mistakes, particularly character names, without inventing dialogue or removing jokes and digressions.
6. **YouTube is the source of truth:** Use the original YouTube video/audio as the authoritative reference. Whisper provides the initial transcription.
7. **Episode-specific speakers:** For Episode 1, use Brendan and Nathan unless the audio establishes another speaker.
8. **Retrospective corrections:** All uncertain attributions can be revised later as more evidence becomes available.

**GOLDEN RULE: Every transcript must be complete, readable, timestamped and fully speaker-attributed. When in doubt, assign the most likely speaker rather than leaving a gap.**

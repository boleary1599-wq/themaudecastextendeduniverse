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

## Transcript reading mode — latest rule
Supersedes earlier visible timestamp requirements: display one clickable checkpoint approximately every five minutes (up to ten minutes where natural). Do not display line-by-line timestamps. Join consecutive caption fragments into readable prose within each named speaker turn. Show speaker names only when the speaker changes. Preserve every original cue and precise timestamp in the underlying TXT/JSON archive for research and future navigation. Do not discard dialogue.

## Episode 003 source
Original video supplied by user: https://www.youtube.com/watch?v=an8PUSgJlb4 (ID an8PUSgJlb4). Archive transcripts/maudecast_ep3.txt; final cue 50:34; page episode-003.html. Embed and caption reading edition committed; named attribution and playback verification pending.

## Episode 004 source
User-supplied original video: https://www.youtube.com/watch?v=rC5CrYN3ENE (ID rC5CrYN3ENE). Raw archive transcripts/maudecast_ep4.txt; final cue 1:02:28. Editorial page and named attribution pending. Video playback not independently verified.

## Episode 004 publication
Page episode-004.html committed with approved Museum Story, Spectral Speculations, The Pleasure of Being Right, compact ledgers, Mauditorium, sponsor status, video rC5CrYN3ENE and 459 caption cues through 1:02:28. Named attribution remains pending; do not describe this as complete. Episode 003 forward link and interior archive updated. Continuity: Kieran competition partner; Stamp 82, stranded 1.5 weeks; Sphinx dumped in local waterway causing flooding; Côte d’Ivoire pop-up and Turkish branch; Uncle Statman John, Stevie D Maude Star, Tom Stray Dog carrier pigeon, Face Forward Simpsons. Maude: Helen alliance, cartoon protest, David protest, mall with sons, retirement-home queue, ages and schooling unresolved. Distinguish conjecture from observed actions.

Episode 004 official title confirmed from original YouTube embed: Itchy and Scratchy and Maude (Maude Cast S1E4). Use official title, not analytical description.

## Speaker-turn boundary rule (25 November 2026)
When attributing dialogue, start a new named speaker at a natural sentence ending or completed thought wherever possible, rather than mechanically at an automatic caption boundary halfway through a sentence. Inspect the surrounding dialogue, split mixed-speaker captions at the actual conversational handover, and preserve every word and original cue in the archive. Genuine interruptions and unfinished sentences may remain where context supports them. Always use the best contextual named attribution; never use Unknown, Unidentified or blank speaker names. Record uncertainty in metadata. Review the finished reading edition for mid-sentence attribution errors before publication.

## Episode 005 source register
Original video supplied by user: https://www.youtube.com/watch?v=tzD6jFeaZ_w (ID tzD6jFeaZ_w). Archived source: transcripts/maudecast_ep5.txt; final cue 1:06:54. Exact title and upload metadata not independently verified; direct video fetch failed. Editorial page pending. For subsequent episodes attempt official channel catalogue discovery before requesting a link from the user; retain discovered video IDs permanently.

## Episode 005 publication and QA
Page episode-005.html committed; video tzD6jFeaZ_w; 498 cues, 130 provisional named blocks, original TXT and attributed JSON. Recaps 183 and 214 words; approved essay The Luxury of Losing Everything retained. Museum: CHAR-MC-YVES-KWAME (14:24–14:38, Côte d’Ivoire manager, message deferred); PLOT-MC-SPHINX prosecution (11:27–12:38); PLOT-MC-STAMP damages $250,000, six and a half days contradicts earlier 1.5 weeks (12:45–14:24); Statman 166 views, dislike, macaroni cheese playlist and kitchen fire (4:21–6:52); Stand by Your Flan (8:40–11:27); Gingham Poofs (1:03:23). Maude: invitation authorship hypothesis (17:36), pharmaceuticals/handedness unresolved (22:31–25:55), Nell shirt hypothesis (34:03), car and marshmallows (35:34), Bible seven cents (43:04), Mary Bailey reference (47:37), alcohol unresolved (49:44). Established MFIMDb mythology, not Simpsons canon: CHAR-MITCHELL-TURNBULL, CHAR-MAGDALENA-TURNBULL, CHAR-REX-TURNBULL, Marilyn Turnbull maiden name; Washington logging village, eight children, parental limb losses, Marilyn seven years as replacement leg, thorny vines, hiking, two additional legs (57:19–1:02:52). Attribution remains cue-level contextual approximation, not verified sentence-level; official title, cumulative Mauditorium, second exhaustive lore pass and live responsive/player testing outstanding. Do not mark complete.

## Mandatory transcript punctuation and readability — 26 November 2026
Before publication, edit every named speaking turn for natural sentence punctuation (full stops, commas, question marks, exclamation marks, apostrophes and appropriate quotation marks), sentence capitalisation, proper names and readable paragraph breaks. Do not mechanically punctuate at caption boundaries. Read across adjacent cues and speaker changes to identify complete thoughts, questions, interruptions and unfinished sentences. Preserve the speaker's wording, humour, hesitations and conversational rhythm; do not paraphrase or invent dialogue. Keep the original timed TXT untouched and retain original cues separately from the edited reading text. Inspect the finished reading edition for run-on sentences and missing punctuation. This is a mandatory publication gate and applies retrospectively to Episodes 001–005. A transcript with named speakers but unedited automatic-caption punctuation fails the gate.

### Episode 006 source registration
User-supplied original video: https://www.youtube.com/watch?v=xxo7nxfvssY (ID xxo7nxfvssY). Original transcript located in Library: Pasted text(20261115-092442).txt. Official title, complete transcript ingestion and editorial production pending. Intended page: episode-006.html.


## Episode 006 checkpoint audit — 26 November 2026
- Source video supplied: https://www.youtube.com/watch?v=xxo7nxfvssY ; archival raw captions `transcripts/maudecast_ep6.txt` end at 59:57. Preserve them unchanged.
- Previous conversation explicitly approved Episode 6 editorial sections: Museum Story, Spectral Speculations / Maude's Life, literary essay **The Woman Who Went to See Aerosmith**, cumulative continuity ledgers, Mauditorium, and the reference to Vivacious. The exact full text of that approved draft is not in this repository or accessible retrieved text; do **not** fabricate an identical reconstruction or overwrite it.
- Audit identified minor factual/speculation corrections, cumulative Mauditorium reconciliation, properly punctuated and naturally paragraphed speaker-attributed full transcript, and official YouTube title confirmation. These remain open, as does deployment and live QA.
- Raw captions themselves contain speech-recognition errors and lines with mixed speakers. Never split mechanically at caption boundaries, assert invented speaker identities, or claim the six-panel publication gate passed without an editorially verified reading edition.
- Episode 006 is **not published** as of this audit. Do not proceed to Episode 007; do not advertise a placeholder as the approved page.

### Episode 006 layout acceptance
Use episode-001.html as structural master, with the existing six panels, deep-purple episode palette, matching embedded video, 5–10 minute clickable transcript checkpoints, original TXT and attributed JSON and return links. Preserve the approved essay verbatim when recoverable; do not silently substitute new text.


### Mauditorium panel border — 28 November 2026
Use a 2px solid orange (#f47c24) outline around the entire Mauditorium panel, retaining its existing purple background, rounded corners, spacing and discovery-first content. CSS: `#mauditorium{border:2px solid #f47c24}`. Backdated to Episodes 1–8 and verified in repository. Live visual QA pending.


### Sponsor credit refinement — 28 November 2026
Sponsors use a restrained double gold outline, subtle purple radial gradient, centered individual bordered credit cards, larger Georgia sponsor names on their own lines, smaller italic existing slogans, a gold heading ornament and a small star below. No invented sponsor content. Applied to Episodes 1–8; repository readback verified, live visual QA pending.

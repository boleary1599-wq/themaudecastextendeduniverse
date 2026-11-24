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

## Episode page editorial layout
Follow MFIMDB-EDITORIAL-RULES.md and MFIMDB-CONTINUITY-GUIDE.md. After the video, show two distinct Story So Far strands (Maudecast Universe and Maude's Universe), a short Literary Essay, the Mauditorium, Sponsor, and Full Transcript. Preserve other episode-specific recurring segments. Use the approved purple episode palette and clear section navigation.

## Separate continuity panels and long-form criticism
Museum Story and Maude's Story must occupy completely separate, individually linked boxes, not subsections of a single panel. Keep the approved purple palette, with orange and gold borders distinguishing the two. Literary essays target approximately 800 words, with a distinct title, thematic subheadings and comfortable long-form typography.

## Naming standard
The independent Maude-universe continuity panel is titled **Spectral Speculations**. It retains both Simpsons canon and clearly labelled speculative lore; the Museum continuity remains separate.

## Episode navigation boxes
Below the video, use individually clickable, responsive menu boxes rather than inline underlined links. Dark purple fill, orange border, gold text, visible hover and keyboard focus; wrap on smaller screens. Use the approved section names, including Spectral Speculations.

## Public continuity narrative voice
Write the Museum Story and Spectral Speculations in a neutral, third-person narrative voice, as an unfolding account of characters and events. Avoid critical commentary, editorial process notes and references to characters who have not yet appeared. Keep literary interpretation in the essay. Do not display timestamps in either public story panel or its continuity ledger; retain source timestamps in internal continuity records and in the full transcript. Clearly distinguish canon from speculation where necessary.

## Spectral Speculations — narrative priority (supersedes earlier public labelling rules)
Lead the Spectral Speculations panel with Maudecast-created biography and developments, ahead of Simpsons background. Within the public MFIMDb story, treat established Maudecast lore as the continuity of this universe: narrate it directly in a neutral third-person voice, without repeated non-canon disclaimers, speculation labels or commentary about the hosts inventing it. Integrate relevant Simpsons background afterwards. Preserve genuine unresolved details without inventing certainty. Internally retain the source classification, original evidence, uncertain claims and distinction between Simpsons canon and MFIMDb canon; the Mauditorium must not present invented biography as verified Simpsons facts. This rule supersedes conflicting earlier requirements for public story-panel labels only.

## Exhaustive factual detail and thematic criticism
Capture ALL recoverable in-universe facts, including obsessive micro-details: every named puppet, pet, fictional programme, object, place, incidental character, exact relationship, number, habit and passing reference. Distinguish a reference or comparison from an established lore fact; retain unclear names for audio verification rather than guessing. The essay is original long-form cultural criticism in the spirit of The Quietus, approximately 800 words. Build a coherent thematic argument with the complete episode transcript as its core and backbone. Draw highbrow and lowbrow references both from within the transcript and from wider culture, connecting them substantively to specific transcript evidence. Never structure the essay as a segment-by-segment recap, checklist, or one heading per podcast item. Use a small number of conceptual headings only when they advance the argument. Revisit evidence across segments to develop and complicate the thesis. Avoid gratuitous references, unsupported claims and invented quotations.

## Autonomous literary essay voice
Treat the transcript as the intellectual source, not the subject of a podcast review. Develop its ideas directly as standalone cultural criticism. Do not name or refer to the hosts, brothers, speakers or their conversational dynamics; avoid formulations such as 'the hosts suggest', 'Nathan observes' or 'the brothers discuss'. Analyse Maude, the mythology, cultural objects and conceptual arguments themselves. Preserve transcript fidelity and internal evidence without narrating the act of podcasting. This supersedes earlier essay examples that foreground host commentary.

## Locked master episode template — Episode 001: Maudtroductions
The approved reference implementation is episode-001.html. Use its structure and editorial approach for every subsequent episode; never copy episode-specific facts into another episode. The required order is: header and episode title; metadata (number, duration, participants); concise introduction; embedded source YouTube video; six clickable navigation boxes (Museum Story, Spectral Speculations, Literary Essay, Mauditorium, Sponsor, Full Transcript); six corresponding content panels; return navigation.
- Museum Story (#story-so-far): neutral third-person narrative of the Museum universe, deep extraction of every recoverable detail, thematic narrative subheadings and cumulative continuity ledger. No public timestamps or critical commentary.
- Spectral Speculations (#maude-story): separate universe and panel, Maudecast mythology first, Simpsons background integrated afterwards, no public non-canon disclaimers, neutral narrative and cumulative ledger. Keep provenance and uncertainties internally.
- Literary Essay (#literary-essay): distinctive title, approximately 800 words, autonomous thematic criticism with the transcript as backbone; high/low cultural references from inside and outside the episode. No host references, conversational recap or segment-by-segment structure. Episode 1's The Importance of Being Nobody is the editorial exemplar.
- Mauditorium (#mauditorium): structured fact register with source timestamps and appropriate provenance; do not confuse invented mythology with verified Simpsons facts.
- Sponsor (#sponsor): document actual sponsor material and relevant lore; explicitly distinguish jokes and unconfirmed sponsorship from confirmed advertising.
- Full Transcript (#episode-transcript): complete named speaker turns, merge consecutive turns, retain timed cues, clickable timestamps controlling the embedded video, optional compact cue display, turn/cue count, downloadable TXT and JSON, honest provisional status and load-error fallback.
- Visual system: deep purple #160f23, cream #f7e6bf, gold links #ffc451, orange #f47c24 header/video/nav borders; 920px main column; dark purple panels; separate orange-bordered Museum and gold-bordered Spectral panels; Georgia essay typography; responsive navigation boxes and mobile layout; accessible focus and skip link.
- Before publication: read the three Bibles, complete two lore passes including obsessive micro-details, reconcile cumulative ledgers, check essay against the autonomous criticism standard, verify navigation/video/transcript functionality and update internal evidence records. Episode 1 is the approved structural and stylistic baseline, not a claim that its provisional transcript has been audio-verified. Its uncertain names and remaining transcription errors must still be resolved. New episode metadata, content, video ID and transcript paths must be independently sourced.


The embedded episode is the viewing control; do not include a redundant Watch on YouTube navigation box. Preserve source links and timestamp functionality.

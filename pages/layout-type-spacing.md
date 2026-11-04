> Generic rules for every client. Client specifics (colours, fonts, world, assets) live in `clients/<client>.md`;
> examples come from Ana Calin's "The Exit Plan" pages (Oct 25 to Nov 4, 2026), where these rules were learned.

# Layout, alignment, type and spacing

Purpose: where things go and how they breathe, so a new client's page reads in one clear order, in her own brand,
on every screen, the first time. Section by section detail lives in [registration-page.md](registration-page.md) and
[vip-page.md](vip-page.md); components in [ui-kit.md](ui-kit.md); wording in [copy.md](copy.md); motion and load
speed in [motion-and-speed.md](motion-and-speed.md); how a page job runs in [page-sop.md](page-sop.md); how Ana's
pages got here in [evolution-ana.md](evolution-ana.md); the selling logic behind section order in
[fladlien-on-pages.md](fladlien-on-pages.md). The "does it look made by Claude?" test is `../graphics.md` §1.

The latest final decision wins. Where something was reversed, the reason is kept only when it teaches.

---

## 1. Before laying anything out

- **One goal decides every layout choice.** On a registration page it is the opt-in. Sean: "Again, our goal is for
  people to get to opt in. That's the goal. Always think of that goal for all devices if you're going to fix their
  UI." On a confirmation page it is the next required action; on a VIP page, the order.
- **No generic "AI pattern" layouts.** No row of three cards with screens, no four-icon feature grid, no stack of
  interchangeable cards. Each section's layout comes from the client's world and the one idea it carries.
  - Sean: "also most of the layouts are generic ai site patterns", then "this looks like an ai pattern landing page
    build".
  - Ana (long offer page, Oct 25): three Dec 30 screens side by side were rebuilt as a December timeline, "Three ways
    December can go", three lanes with Christmas week shaded. The four-icon "Everything inside" grid became a product
    illustration beside a plain list.
- **One focal point per section.** One main graphic that acts out the section's point, at most two props, clear
  margins (`../graphics.md` §1, [registration-page.md](registration-page.md) §3).
- **No two sections share a layout.** Vary how sections open (some centred, some left) and remove decoration that
  repeats without adding information. Sean: "The UI right now is a little bit generic-ish and repetitive."
  - Ana VIP: the week and the fit check open centred; a decorative VIP lane under the week and a repeated stamp strip
    were removed.
- **Prefer compact.** When a page feels heavy, tighten it; never add blocks to fix it. Sean: "too bulky".
- **A reference gives density, never identity.** Borrow how compact a reference is, then build it in the client's
  brand, and make sure it does not look like the other pages we made either.
  - Sean on Ana's short offer page: "I like the compact vibe of Jay's offer short page... I want this offer short page
    to be compact". Path: "still looks too much like Jay's", then Claude's Ana version was "too bulky" and "too much
    like every other page that we made", then Claude reverted to Jay without being asked ("I didn't tell you to
    revert it"). Final: the receipt first screen kept, the lower half in Ana's look made compact (two weeks per row,
    four reader notes per row, a swipe row on phones), about 7,240px tall instead of about 10,000px.
  - Lesson from the revert: never undo work as an answer to "make it better"; improve what is there.

## 2. Keep an approved layout; tighten it, don't restructure it

- **Once Sean approves where things sit, those decisions stay.** Later rounds raise the finish, not the placement.
  Sean on Ana's VIP redesign: "I liked the areas where you put the design, like the decisions are right. Now we have
  to elevate the design".
- **A fold or crowding problem is fixed by tightening first:** thinner column, smaller gaps, a compact card, then a
  slightly smaller headline on short screens only. Never centre or stack an approved two-column hero to win space.
  - Ana, Nov 4: Claude centred the hero with everything under the video; Sean: "Is it even a good idea to put it in
    the center? ... Shouldn't we keep it the same layout, but thinner, of course?" Full order of fixes:
    [registration-page.md](registration-page.md) §5.6.
- **When Sean compares two versions and picks the old one, restore it exactly.** Ana's confirmation top: "Your seat is
  saved, [Name]. Four quick steps before you go." (VIP: "You're VIP, [Name]. Four quick steps before you go.") with
  the line listing the four steps. A new top was tried; Sean: "ok i like the before".
- **Keep the charm:** improve on top, never strip a page to rebuild (README rule 7).

## 3. Left-align or centre?

- **Left-align anything people read:** paragraphs, lists, form labels, question lists, bullets, step text. Long
  centred paragraphs are not used.
- **Centre short openers only:** an eyebrow plus a heading plus one line, on sections chosen to vary the rhythm (Ana
  VIP: the week and the fit check). A centred opener is followed by left-aligned content.
- **A hero with text beside a graphic is left-aligned and two columns.** It is never centred on desktop or laptop.
- **Never right-align long paragraphs.** They are hard to read. Sean offered "You can probably send some text on the
  right side, right-aligned, or maybe full width"; full width won (section 6, the split pattern).
- **Justify only on tablet and desktop,** and only body paragraphs in side-by-side or two-column sections, so they
  reach the right edge cleanly: `text-align:justify; text-align-last:left; hyphens:manual`. Phones stay left-aligned:
  justified text leaves big gaps in highlighted lines.
  - Ana: `.bring-tx p:not(.bring-that)` justified from 601px ("Why attend live").
- **A badge or logo beside a heading sits as two columns, not stacked above it:** badge left, then pills, heading and
  text left-aligned on the right. On phones it stacks and centres with the badge smaller.
  - Sean: "That's a little bit too big ... I want the logo to be beside the header, beside the "Answer 7 Quick
    Questions," like two columns."
  - Ana confirmation step 4 (`.cxs-h:has(.cxs-ht)`): `grid-template-columns:168px minmax(0,1fr)`, gap 34px,
    max-width 900px, badge 168px (was 200px); at 760px and narrower one column, centred, badge 128px.
- **Floating helpers sit out of the reading line.** Ana: the sticky Day 1 to 3 tracker (`.dmap`) is centred on
  phones and moves to the top right on desktop (`justify-content:flex-end; top:96px`, scaled .82 from the right edge,
  from 1061px). Sean: "can you put this floating thing for days 1 to 3 under the top-right side instead".

## 4. Column structures

### 4.1 Hero (registration)

- Two columns: the visual (host video in a scene from her world) left and wider, copy and form right. Sean: "I want
  the column of the video to be bigger than the text column, just like before."
  - Ana: `.v2h.hgrid{grid-template-columns:minmax(0,1.52fr) minmax(0,1fr)}` from 1061px, gap 40px (started at about
    1.44fr / 1fr and grew with the video window). Claude's 1.1fr / 1fr to fit a bigger headline was reversed.
- No second column of text in the hero. Sean: "I don't like this idea about two-column text".
- Never a narrow headline-plus-form column: the right column must be wide enough for a big headline.
- One clear order on the copy side: small pill, big headline, sub line(s), then the form. Nothing scattered around
  the hero. Sean: "The text placements are very wrong. They don't have hierarchy. Everything's all over the place."
- Full spec: [registration-page.md](registration-page.md) §5.

### 4.2 Frozen side form (long registration pages)

- Page content left, a slim form column frozen on the right once the hero form scrolls away, so content keeps most of
  the width. Sean: "I want to freeze the form on the right side... I want to stick with the two-column layout... Since
  Anna's form is simpler, we can make it thinner, slimmer, so there's more surface area for the page content itself."
- Ana: `aside.v2rail` from 1280px, `--rw:284px` wide, `--rg:44px` gap; page content keeps its right margin so nothing
  runs under it. Tried first as a noindex trial at `/v2/` with the live page untouched, then became the main page.
- At 1280px the headline must sit clear of the frozen form. Below 1280px there is no rail.
- Details and behaviour: [registration-page.md](registration-page.md) §5.8, [ui-kit.md](ui-kit.md).

### 4.3 Rows with a screen or picture beside text

- **Text beside a mockup:** no empty gap on the text side. Centre the text block vertically against the screen, make
  the screen panel a little smaller, set the type slightly larger, and fill the space with useful items (three ticked
  steps, a progress bar, what you keep), not a long paragraph. Phones: words first, then the screen.
  - Sean: "kinda prefer this layout byyt make it better" (one row per week, words left, screen on a dark panel right,
    over a two-per-row grid).
  - Ana /join weeks: three ticked steps, a December bar (earlier weeks filled, Christmas week shaded, this week
    yellow), "You keep" with the sunflower.
- **Split pattern for a tall picture beside a lot of text:** beside the picture only the eyebrow, heading and first
  lines (the hook); the picture sized to that text column's height; then a dashed divider; the rest of the
  paragraphs in two even columns across the full width; then the button. Phones: one column under the picture,
  tight gaps. Sean: "still too much awkward white space in between". Spec and Ana's sections ("Why attend live", the
  gift): [registration-page.md](registration-page.md) §3.2.
- **Use empty space on the right.** When a row leaves a wide empty area, let the top of the text run across both
  columns. Sean: "You can probably widen some text on the top here since there's still a lot of space on the right."
  - Ana day rows (from 1061px): `.drow` grid `72px minmax(0,1fr) minmax(0,1.08fr)`, gap 0 44px; the date, the `h3`
    (max-width 15.5em) and the first paragraph (max-width 40em) span `grid-column:2 / 4`; the slides window sits
    beside the bullets and stays in view (`position:sticky; top:170px`). Flipped rows mirror it. 1060px and narrower:
    stacked.

### 4.4 Task first, reward second (confirmation and tool pages)

- The action people must take leads and gets the wide column; a teaser of the reward is a small side panel. Sean:
  "The survey observation is the first thing they would see. I think the calculator UI is a little too big." Then:
  "Actually, make the survey a little bit bigger in width."
  - Ana confirmation step 4: from 1000px `.cxs .wrap{max-width:1160px}` and
    `.cxs-g{grid-template-columns:minmax(0,1fr) 340px}`: survey about 742px wide (was 633px), calculator preview a
    fixed 340px column under the progress bar. Phones: questions first (first question moved up about 110px), preview
    after.
- **Steps in a row:** Ana's confirmation steps are three columns from 1000px (`repeat(3,minmax(0,1fr))`, gap 20px),
  the middle one wider for the email demo from 1100px (`minmax(0,1fr) minmax(0,1.3fr) minmax(0,1fr)`, max-width
  1072px). Small pink circle arrows sit between cards and turn to point down when cards stack (999px and narrower,
  `transform:rotate(90deg)`).
- **A section with one or two cards gets its own layout,** never a grid built for more that leaves empty columns.
  Sean: "why does this look like this" and, on VIP, "Also, what even is this layout here?"
  - Ana: `.acts.one` from 861px: one card, max-width 1000px, `grid-template-columns:minmax(0,1fr) minmax(0,.85fr)`,
    column gap 48px, words and button left, the sheet right. VIP "Then two small things.": paired cards run full
    width, each with words and button left and the picture right.
- **A long tool becomes numbered steps,** each in its own matching colour, each opening with a "Goal:" line, a short
  note on why it matters, and a status line when collapsed. Add an optional last step for later. Sean: "Add an actual
  goal in every part."
  - Ana /exit-number: "Goal: find out how much of each sale you actually keep.", "Goal: see if this plan fits the
    hours you really have."; status lines like "You keep $475 a sale" and "Over by 4.7 hrs a month"; last step
    "Later: record what really happened".
- **Short offer page (for people who just watched the pitch):** on desktop the order card sits beside "what's
  included" and stays in view; on phones the order card comes first so they can pay straight away.

## 5. Type

### 5.1 Faces

- **Serif (the client's display face) for big headlines only:** H1, section H2, day headings, pull quotes.
- **Sans for everything read and every number:** body, sub lines under a headline, question lists, lists, labels,
  form headings, buttons, prices, stats, letters and other long reads. Sean on the VIP letter: "You should use sans
  serif for this one".
  - Ana: `--serif:'Instrument Serif'`, `--sans:'Manrope'`; `h1,h2,h3{font-family:var(--serif);font-weight:400;
    letter-spacing:-.012em}`.
  - Ana's "What if..." question list in "Why attend live" is in the sans.
  - Names under pictures are sans too, bold, never the client's handwriting face. Sean: "use sans serif for their
    names" (Ana's conversation prints first had the names in her handwriting; now Manrope 800, `.convos li b`).
- **A named tool inside a serif heading switches to the sans,** bold, in ink, with a highlighter that is not the
  accent, so it reads as a product. Sean: "can you make the word 'exit number calculator' sans serif instead of
  serif?... Also, a different color, not pink".
  - Ana: `<span class="cxs-k">to unlock your <mark>exit number calculator.</mark></span>`, `.cxs-k` sans 800 at .6em,
    the `mark` in sunflower yellow (`linear-gradient(transparent 52%,var(--sun) 52%,var(--sun) 94%,transparent 94%)`),
    the same highlighter device as "in 2027" on the main page.
- **Never a fake italic.** If the face has no real italic, emphasise with bold in the accent colour.
  - Ana: the hero sub line's question phrase stays pink and bold, not slanted.
- **The client's own fonts.** A display face from her own slides can carry a big headline with her highlighter
  (Ana's Bonny was tried in an editorial hero on Oct 31; that hero was dropped, the rule on her own fonts stands).
- **Load every font a graphic uses and check it renders.** A handwritten note must never fall back to a plain serif
  (Ana's calendar note and "my price?" once showed in a serif because the handwriting font was not loaded).

### 5.2 Scale (Ana's values; scale to the client's faces)

| element | rule | Ana |
|---|---|---|
| Hero H1 | the loudest thing on the first screen, as big as its column allows | `h1.h1x{font-size:min(13.4cqi,84px);line-height:1}`, about 69px at 1440; phones `min(14.2vw,60px)`, about 55px at 390 |
| Hero pre-line | about half the H1, proof number highlighted | `.h1a` at `.46em`, `$1.4M` in `.hl` |
| Line under the H1 | sans, bold, about 17 to 19px | `.hlead{font-family:var(--sans);font-weight:700;font-size:min(3.6cqi,19px)}`, 17px on short laptops |
| Section H2 | serif, big | `h2{font-size:clamp(40px,4.6vw,64px);line-height:1.02;text-wrap:balance}` |
| Day heading | serif | `.dtext h3{font-size:clamp(38px,3.6vw,52px);line-height:1.02}` |
| Section question in a dense section | serif, large | `.who .iq{font-size:clamp(34px,3.7vw,54px);line-height:1.1}` |
| Intro line under it | large sans | `.who .ilead{font-size:clamp(25px,2.2vw,31px);line-height:1.3}` |
| Body | sans 17 to 18px, line-height 1.6 to 1.72 | `body{font-size:17px;line-height:1.6}`; `.who` paragraphs 18px / 1.72 |
| Small notes | never below about 15px, normal text colour | `.who .inotes p{font-size:15.5px;color:var(--ink2)}` |
| Eyebrow | sans caps, 800, wide tracking, accent | `.eyebrow{font-size:13px;font-weight:800;letter-spacing:.16em;text-transform:uppercase;color:var(--pink)}` |
| Form heading | sans 800, one line | `.tk-h` "Save your free seat", 36px, `white-space:nowrap` (31px on short laptops) |

- **"Make the header bigger": confirm which heading.** Twice it meant the page H1 and Claude enlarged something else
  (the form heading, then the "Why attend live" heading). Sean: "Wait, I meant the heading of the page" and later
  "i said you can make this bigger". Measure against the headline element itself.
- **Big, but contained.** The H1 never fills the full page width, never leaves big white gaps, and never runs under
  the frozen form. Ana's editorial hero at about 100px full width was too big; Sean: "There's too much white space
  going on in the header headings."
- **Size a headline to its real text width** (measure the text, `width:fit-content`), not the box, so no empty space
  sits beside it.
- **Split a heading that runs to five lines:** a main line at full size plus a smaller sub line.
  - Ana: `h2.bring-h` (`clamp(34px,3.4vw,50px)`) with `.l2` at `.56em`, `text-wrap:balance`.
- **Never shrink type to make a dense section breathe** (section 7). Sean: "Isn't the text size a little bit too
  small?"

### 5.3 Bold and highlight

- **Bold only the sentences that matter.** The key line of each section is bold and swept with the brand's
  highlighter; related sentences carrying the same information are bold too. Sean: "the stuff you put in bold is not
  really even that important. You can make the sentence bold, and the other sentence that relates to this is similar
  in terms of information. not just highlight, bold too".
  - Ana: bold plus highlight on "Put that question in our private VIP WhatsApp group" and on the VIP hero offer
    sentence "For $67, add lifetime workshop recordings...".
- **No decorative bold:** not feature names, not rhetorical lead-ins, not "No." / "Yes." at the start of FAQ answers.
- **The highlighter is subtle:** a lighter tint of the brand accent covering only the lower part of the line. Sean:
  "make the highlight a bit subtler".
  - Ana inline highlights: `rgba(255,212,0,.42)` sitting on the lower part of the line, e.g. `.fit .fix span`
    (34% tall, sweeps in on select) and the day headings `.dtext h3 .dh` (`transparent 58%` to `90%`).
  - Day headings: "Find the *people your business could serve*.", "Find the *part of what you know* that *could
    become your business*.", and "path" on Day 3. Sean: "subtly highlight 'part of what you know' and could become
    your business".
- **A solid highlight is kept for one or two hero marks only,** e.g. Ana's proof number `$1.4M` in `.hl`
  (sunflower `var(--sun)` from 14% to 94%).
- **Reuse the same highlighter in video and graphics** so the page and film match (Ana's yellow sweep under key
  words; `../video-editing.md`).
- **Numerals for key counts** in body copy, kept on one line: "three (3) free, live sessions" (`.nn{white-space:
  nowrap}`; [copy.md](copy.md)).

## 6. Line breaks and line length

- **Headlines are hand-broken on whole phrases,** with separate breaks for phones (more, shorter lines so the type
  stays big). No small word ("the") hanging at a line end, no split verb phrase, no lone orphan, the year never
  splits, a number never splits from its unit ("7 purchases" stays together). Sean: "looks a bit awkward. how to fix
  the line" and "fix per line".
  - Ana H1 now: pre-line "My Newsletter Business Has Made $1.4M.", then "Here's What I'd Do First / If I Wanted to
    Leave / My Job *in 2027*." (`.h1b .l` lines, `white-space:nowrap`); phones five lines with `.h1b .m{display:
    block}` forcing key words onto their own line.
  - Earlier Ana H1 (Nov 2), the break pattern still worth copying: desktop "How to Build the Business / That Pays You
    for / What You Know *in 2027*", phone "How to Build / the Business / That Pays You for / What You Know / *in
    2027*" at about 52px.
- **Check every multi-line heading at every width.** Ana's gift heading "How many sales would you need to reach your
  monthly income goal?" was fixed to break on whole phrases at each width.
- **Balance short wraps** (`text-wrap:balance`) so an intro never leaves one word alone on its last line (Ana's
  "Everything inside" intro once left "you." alone).
- **Short labels never wrap inside:** dates, times, prices, pills. A crossed-out pill never wraps onto two lines;
  "·" ends a line, never starts one (`../graphics.md` §6).
- **A bold lead-in never breaks its bullet into one word per line** (Ana's "Copy, count, pick:" bug).
- **When a hidden line break joins two words, keep the space** (it once rendered "PLANEYES").
- **Line length:** text blocks get a set width so lines never squeeze and the text always fits its box.
  - Ana: `.who .itx{max-width:640px}`, day heading 15.5em, day first paragraph 40em, `.bring-h .l2 em` 26ch, the
    "who" question 900px.

## 7. Spacing and rhythm

- **Even, calm gaps;** nothing cramped, nothing stretched. Sean: "Some of them are too scattered. Some of them are too
  tight. Make it more balanced. Sometimes the text doesn't fit in where they are."
- **Section padding (Ana):** registration `section{padding:120px 0}` on desktop (88px and 76px at smaller widths);
  VIP `section{padding:110px 0}` (84px, then 72px on phones).
- **A heading gets clear room below a dark band above it** (Ana's "Everything inside" heading once crowded the band).
- **A hero graphic gets breathing room** and never touches the strip above it (Ana's shutter tops once touched the
  trust strip).
- **A pointing arrow sits close to what it points at.** Sean: "a little bit too far from the arrow" (Ana: the gap
  from the arrow to the step 4 badge roughly halved on desktop).
- **A reference line sits tight under the thing it pairs with,** no extra margin (`../graphics.md` §6).
- **Dense text beside a sticky form: add air, never cut content, never shrink the type.** More space before the
  content, between paragraphs, before the button and notes; a shorter line length; the photo aligned to the top of
  the text; lighter marks. Sean: "I don't want to remove anything. I just need to be able to breathe because there's
  a lot of text."
  - Ana "who" section (`.intro.who{padding:120px 0 116px}`): question up to 54px, then 76px gap; intro line up to
    31px; paragraphs 18px with 18px between and 26px before the second; button 36px below; notes 15.5px, 52px below
    with 30px padding. A first pass shrank the type (46 / 27 / 16.5 / 14px) and was sent back.
- **Size a picture to the text beside it** instead of stretching gaps to fill a tall picture (section 4.3).
- **Keep a gap tied to the art's size** when art scales: Ana's booking strip `margin-top:calc(13.7% + 34px)`, the
  same visual gap at 1100, 1280, 1440 and 1920.

## 8. Balance and white space

- **No awkward white space** beside a headline or on one side of a section. Fill a lopsided section by splitting the
  text into full-width columns (section 4.3), by letting the top run wider, or by tightening, never by stretching
  gaps or right-aligning paragraphs.
- **Pictures:** one main device, two props, clear margins, nothing on top of text (`../graphics.md` §1).
- **Fit-to-content strips are centred over what they belong to,** not stretched to the column. Ana's trust strip
  `.tstrip{width:max-content}`, centred over the video window (about 560px).
- **A pull quote is attached to the section it introduces,** never floating in its own band with a gap above it.
  Sean: "is this supposed to be like this?" (Ana VIP: the quote now opens the fit check on the pink ground, then a
  short divider; [vip-page.md](vip-page.md) §9).
- **Decoration that makes the first screen feel heavy moves elsewhere.** Sean: "these can be moved maybe on the footer
  instead so it wont look overwhelming." (Ana's village skyline moved from the hero bottom to the footer's top edge.)

## 9. Never cover text

- Nothing sits on top of text: no prop, stamp, sticker, note or glow.
- Test overlays with the longest real name. On phones a stamp goes on its own line above the label (Ana: the stamp
  once covered "Christina's").
- A coloured bar never straddles the seam where two section colours meet: extend the section colour so the bar sits
  on one ground (Ana VIP confirmation: the pink starts at the very top).
- Info pieces and graphics sit in free space, above scenery, never buried (`../video-editing.md` §5).
- **Still to do (judges, Nov 4):** on Ana's page the day map covers text in the Day 2 row.

## 10. Grounds and backgrounds (layout side)

Full rules: [registration-page.md](registration-page.md) §23, [vip-page.md](vip-page.md) §16, `../graphics.md`.
- **Calm, light ground.** Very light warm tones, never mid grey. Sean: "also make the grey bg a bit lightwe" (Ana
  offer pages: `--ground:#F3F0EB; --ground2:#F9F7F3; --paper:#FFFDF9`). Main pages: cream `--cream:#FFF8EE`;
  VIP `--page:#F8F3EB`.
- **Flat and clean; no page-wide grain.** Sean: "I still don't really like how the background looks. It looks a little
  cheeky". Texture lives in pictures and as faint, per-section textures made in code.
- **Colour in shapes and section moods, not big flat fills.** Sean: "Not a fan of this background color", "plain white
  background, but we can probably add some flare sometimes".
- **One background idea per section, tied to its meaning;** it adds fun without changing the layout. Sean: "Not just
  colored shapes, but actually think of a unique background for that specific section."
- **Grounds come from the client's fresh palette tints;** no muddy beige or grey, no grey texture overlays. Sean: "im
  not a fan of this puke poop grey color they dont really go well". Ana: cream default, sunflower cream `#FFF1C9`
  for "Where are you right now?", blush for "A life left to enjoy it".
- **A background metaphor must read at a glance.** Faint lines that do not read as the thing are replaced. Decorative
  connectors hide on phones when cards stack (Ana: the three roads in the picker are hidden on phones).
- **Matching sections across a funnel share the same finish** (Ana: the yellow footer carries the same grain on the
  registration and VIP pages).

## 11. Laptop heights

- Check 1280x720, 1280x800, 1366x768, 1440x900, 1536x864, 1680x1050, 1920x1080.
- The visual is fully in view; headline, sub line and most of the form are in view. The button may sit slightly below
  the fold on short laptops only when a floating header button is always in view.
- Trim by height, not by width: Ana `@media (min-width:1061px) and (max-height:830px)` sets the H1 to
  `min(9.4cqi,56px)` and the line under it to 17px (1366x768, 1280x720); `max-height:760px` goes to
  `min(8.8cqi,50px)`. At 900px tall the H1 stays full size. Sean, on keeping it big: "i said you can make this bigger".
- Full order of fixes: [registration-page.md](registration-page.md) §5.5 and §5.6.

## 12. Big monitors

- From about 1800px wide, scale the whole page up evenly so it fills the screen like it does at 1440. Keep 1440 to
  1920 as is. Never scale up on laptops (it pushes the form down). The form must still fit on the first screen and
  the side form must still follow on scroll. Sean: "Yeah, I think we can scale for big monitors, for sure."
  - Ana: CSS `zoom` set by a script in the `<head>`, `k = min(w/1600, h/1075, 2)`, ignored under 1.05; lengths tied
    to the screen are divided by `--z`. Details: [registration-page.md](registration-page.md) §5.7.
- **Still to do:** Safari handles `zoom` differently; Ana's page is checked in Chrome only.

## 13. Phones and tablets

- **Work in passes:** desktop and laptop first, then phones and tablets (portrait AND landscape), then every device
  (Android vs iPhone). Sean: "But for now, we're going to optimize the desktop and the laptop." and "if it's portrait
  for the tablet or if it's landscape, you should also think of that".
- **Registration hero on phones:** one column; pill, headline, sub line, then the form with its button on the first
  screen, then the video and the rest ("see the form ASAP"). Desktop-only extras (booking strip, drawings, the frozen
  rail) are hidden; a bottom bar keyed to the hero form carries the CTA. Detail: [registration-page.md](registration-page.md) §25.
- **VIP hero on phones:** the video stays visible, the order card right under it ([vip-page.md](vip-page.md)).
- **Rows become readable rows:** Ana VIP week reads as rows (picture left, words right); each VIP item one column.
- **Wide timelines and comparisons stack** each lane with its result on top, so nobody swipes sideways to find the
  outcome. Where a swipe row is used, add a phone-only hint and dots (Ana /program: "Swipe through the month.").
- **Text beside a screen:** words first, then the screen. Task before reward (survey before calculator).
- **Badge beside a heading stacks** with a smaller badge (Ana 128px). Justified text goes back to left-aligned.
- **A frame sized by its image needs an explicit width** once the image is moved or replaced, or it collapses to zero
  on phones (a blank phone screenshot was the clue on Ana's page).
- **Mid widths matter:** check about 900 and 1100px; button text must never spill out of its card (Ana's WhatsApp
  button did at both).
- **A row of small pictures steps down evenly:** Ana's conversation prints are 6 across on desktop, 3 at 1060px and
  below, 2 at 640px and below (`.convos .cv-row`, `repeat(N,minmax(0,1fr))`), so every frame stays big enough to
  read a face.
- **Side-by-side lines stack on phones:** Ana's final date line puts the visitor's dates first and New York's beside
  them on desktop, under them at 640px and below (`.ftimes .ft-d .ft-ny`).
- **Still to do:** Ana's phones and tablets pass. Sean: "there's also some stuff that looks weird on phone, like the
  graphics and the layout, so we can probably fix it and make them more mobile-friendly." Also the brick wall on the
  confirmation page breaks out of view on phones; a small strip of it above the questions was offered, no answer yet.

## 14. Checks after every change (before saying done, before every publish)

- **No sideways scroll at any width from 320 to 1920px,** tablets around 1024 included, and when an input takes
  focus. Check `scrollWidth > innerWidth` at 320, 390, 1024, 1280, 1440 and 1920; screenshot 1440, 1280 and a phone.
  Common causes and fixes:
  - tilted photos, absolute notes, glows, confetti: `overflow-x:clip` on the section;
  - grids: `minmax(0,1fr)`, never bare `1fr` with wide content;
  - `nowrap` meta spans: put breakable spaces between the chunks;
  - a scroll on focus: `overflow:hidden; overflow:clip` (Ana's `/exit-number` `.xmain` shifted on focus with
    `overflow:hidden` alone).
- **Every date window:** before open, live days, open, closed. No colliding labels; rings and marks centred on their
  target (Ana: a calendar ring once sat under the 30th instead of around it).
- **Phone CSS is not overridden by later desktop CSS** (Ana's week rows once stayed two columns on phones).
- **Accessibility and mobile basics:** controls at least 44 x 44 CSS px, keyboard access, persistent labels, visible
  focus, labelled errors, reduced motion respected, never colour alone for a status, readable zoomed and printed.
- The SOP check list: `../SOP.md` §B.5.

## 15. Still to do and open

- **Still to do:** Safari check of big-monitor scaling (section 12).
- **Still to do:** phones and tablets pass on Ana's registration page (section 13).
- **Still to do (judges, Nov 4):** on a 320px phone the form heading "Save your free seat" runs past the edge; the
  phone bottom bar overflows at 390 and 320px; the frozen side form breaks "About 90 minutes a session" across lines;
  the day map covers text in the Day 2 row (section 9).
- **Open:** the brick wall strip on phones (confirmation page).
- **Resolved:** "usesans srif here" (Oct 31, 11:56) was the line under the hero H1 (commit c2dcbc7 set it in the
  sans). The standing rule covers it: sans for anything read, including the line under an H1 (section 5.1).

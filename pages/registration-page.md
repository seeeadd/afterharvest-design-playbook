> Generic rules for every client's registration page. Each rule is written so it carries to any client in their own
> brand; Ana Calin's "The Exit Plan" page (https://exitplan.howwegrowtoday.com, `index.html` in seeeadd/2026-ana-calin)
> is the worked example, with exact values, copy and selectors. Her facts live in `../clients/ana-calin.md`.

# The registration (opt-in) page, section by section

**Purpose:** one page that gets the right people to put their first name and email in, for a free live event. Every
section, graphic, line and animation is judged by one question: does it help them opt in?

Read with: [page-sop.md](page-sop.md) (how a page job runs), [layout-type-spacing.md](layout-type-spacing.md),
[ui-kit.md](ui-kit.md) (header, forms, buttons, tickers, popup), [copy.md](copy.md),
[motion-and-speed.md](motion-and-speed.md), [fladlien-on-pages.md](fladlien-on-pages.md),
[vip-page.md](vip-page.md) (the page right after this one), [evolution-ana.md](evolution-ana.md) (how Ana's page got
here, version by version), and the house files `../graphics.md`, `../motion.md`, `../SOP.md`.

Status words used below: **final** (Sean approved or it stood unchallenged and shipped), **still to do** (known gap),
**open** (waiting on Sean or the client).

---

## 1. The goal

- **One goal: the opt-in.** Sean: "Again, the purpose of this page is to get them to opt in. That's it." And, for
  every device: "Again, our goal is for people to get to opt in. That's the goal. Always think of that goal for all
  devices if you're going to fix their UI."
- **Two jobs for the page to do that:** make the event easy to understand (what, when, where, free, for whom), and
  make people curious about this specific event (what they will learn that they can't get elsewhere).
- **Never at the cost of honesty.** No invented counts, results, values, scarcity or "people registered" lines. Proof
  is real or it is left out (section 22, and `../SOP.md` E).
- **No fluff.** Every block carries a concrete, specific point. "everything still needs a detailed refresh. still
  looks like a draft, well it is."
- **Not a template.** No generic "AI pattern" layouts (3-column card rows, four-icon feature grids, interchangeable
  card stacks). Sean: "this looks like an ai pattern landing page build". Each section gets a layout that comes from
  the client's world and the one idea it carries, and neighbouring sections never share a treatment ("everything
  looks about the same").

## 2. The order of sections, and why

The order follows the client's latest copy doc. Sections that are not in the latest copy are removed, even
when they looked good (Oct 31 rule; on Ana's page that removed "What you won't hear from me", the "Likes are
lovely" band, the 2015 to 2026 host timeline, the old WHAT/WHEN/WHERE tiles and a scrolling review wall). Never drop
existing proof cards in a copy update unless Sean says so (section 8).

The general order, with the buyer question each step answers:

| # | section | buyer question it answers | Ana's selector |
|---|---|---|---|
| 0 | floating header | what is this, when, is it still open? | `.fb` |
| 1 | hero | what is it, who runs it, why should I care, how do I get in? | `section.hero` |
| 2 | opening ("you want to know...") | is this about my situation? | `section.intro.who` |
| 3 | the three days, then "come to all three" and the featured result | what will I actually learn, day by day? does it work? | `section.days` |
| 4 | situation picker ("Where are you right now?") | is it for someone like me? | `section.sand.where` |
| 5 | host story, then the people she has learned from | why her? who backs her? | `section.host`, `.convos` |
| 6 | why attend live (live review) | why live, not a replay? | `section.bring` |
| 7 | the gift (calculator) | what do I get just for signing up? | `section.gift` |
| 8 | fit check ("Wherever you're starting...") | my objection is covered? | `section.sand.fit` |
| 9 | reviews and wins | do students rate her? | `section.revs` |
| 10 | prize draw | why stay to the end? | `section.prize` |
| 11 | FAQ | is it really free, how much time, what's the catch? | `section.qa` |
| 12 | recap / closing ask | the whole thing again in one breath | `section.sum` |
| 13 | final invitation ("See you live.") | when exactly, in my time zone? | `section.sand.final` |
| 14 | footer, popup form, exit popup | | `footer`, `#modal` |

Why this order:
- **Promise before proof before price of time.** The hero states the promise and the date; the days show the
  mechanism; results follow the days, so they read as what the days lead to.
- **Self-selection early.** The opening and the situation picker let people see themselves before the host story.
- **Host after the mechanism.** People care who she is once they want what she teaches.
- **Gift and prize late.** They are reasons to act now and to stay, used where attention dips.
- **Objections near the end** (fit check, FAQ), then a short recap, then one calm final invitation with the times.
- **Check the buyer questions in this order** on every new page: is it for me, what do I end up with, will it work
  for me (students' results, not praise), how much time and when, how much of the host do I get, where it happens and
  what I keep, tools needed, what if it doesn't work, what happens after I click, why now.

## 3. Rules that hold in every section

Short versions; the full rules are in the linked files.

- **Layout:** one focal graphic per section that acts out the section's point, plus at most two props, clear margins,
  nothing on top of text (`../graphics.md` §1, [layout-type-spacing.md](layout-type-spacing.md)). Sean: "Some of them
  are too scattered. Some of them are too tight. Make it more balanced. Sometimes the text doesn't fit in where they
  are."
- **No awkward white space** beside text or headlines; fill a lopsided section by splitting the text (section 3.2
  pattern below), not by stretching gaps or right-aligning paragraphs.
- **Type:** serif for big headlines, sans for everything read, numbers, question lists and sub lines. Body 17 to 18px
  (Ana: `body` 17px, the dense reading sections 18px; [layout-type-spacing.md](layout-type-spacing.md) section 5.2).
  Never a fake italic: if the face has no italic, use bold in the accent colour.
- **Bold and highlight:** the key line of each section is bold and swept with the brand's highlighter as it scrolls in;
  related sentences carrying the same information get bold too; no decorative bold ([copy.md](copy.md)).
- **Line breaks:** headlines are hand-broken on whole phrases, separately for desktop and phones; no small word
  hanging at a line end, no number split from its unit, the year never splits. Sean: "fix per line". Check every width.
- **Numerals:** key counts in body copy carry the numeral in brackets on one line: "three (3) free, live sessions",
  "two (2) copies", "seven (7) quick questions" (`.nn{white-space:nowrap}`).
- **One CTA per section,** first person, with the word free (section 21).
- **Facts change everywhere at once:** a new day title, date or claim is changed on every page and inside every
  picture that shows it (slide thumbnails, recording cards, alt text), keeping the same illustration.
- **Fonts load or the graphic fails:** every font a graphic uses is loaded and checked; a handwritten note must never
  fall back to a plain serif (Ana's handwriting font was missing once, and "my price?" showed in a serif).
- **Mock app screens show the event itself:** a calendar, inbox or chat on the page shows the event's real dates and
  number of days, not the host's ordinary week. Sean: "Fix the calendar here. Update the dates. Why is it 5 days? It
  should be 3."
- **One accent across the funnel:** every page of one client's funnel and the mock screens inside them use the same
  accent; third-party things shown as examples keep their own colours.
- **Brand marks are traced** from the client's real logo file, never redrawn by eye (`../graphics.md` §3).
- **Speed is part of the design:** keep every graphic and animation, make them cheap ([motion-and-speed.md](motion-and-speed.md)).

### 3.2 The split pattern for text beside a picture

Used when a section has a tall picture beside a lot of text (Ana: "Why attend live" and the gift). Sean: "still too
much awkward white space in between".
- Beside the picture: only the eyebrow, the heading and the first lines (the hook). Size the picture to that text
  column's height.
- Then a dashed divider, then the remaining paragraphs in two even columns across the full width, then the button.
- Body paragraphs in those columns may be justified on tablet and desktop only (`text-align:justify;
  text-align-last:left`, Ana from 601px). Phones stay left-aligned: justified text leaves big gaps in highlighted lines.
- Phones: one column under the picture, tight gaps.
- Never long right-aligned paragraphs. Sean offered "right-aligned, or maybe full width"; full width two columns won.

---

## 4. Floating header (summary; full spec in [ui-kit.md](ui-kit.md))

- **Purpose:** keeps the event, the date, the visitor's own time and the button in view on every scroll position.
- **Content:** brand cartoon, event line ("The Exit Plan · A free 3-day live event with Ana Calin"), dates, New York
  time, the visitor's own date, time and city when it differs (theirs leads, bold with a soft highlight; New York
  smaller and grey underneath), a "Starting soon" countdown, and the button "I'm in, Ana (it's free)".
- **Shape:** a floating frosted-glass card with depth that slims on scroll; never a flat grey bar.
- **Rule:** the "free 3-day live event" words are never removed from the header.
- **Tab icon:** the host's cartoon as the favicon, cropped tight on the face at 16 and 32px, the full mark at
  home-screen sizes (Ana: the sunflower version here; the crowned pink version only on the VIP pages).
- **Phones:** a bottom bar replaces it (`.mbar`). Since Nov 4 the bar shows the visitor's own dates ("The Exit Plan ·
  Dec 9 to 11" in Manila). **Still to do:** it still has no time or city (Sean: "Shouldn't the phones also have the
  date line? Isn't that important?"), and the judges found it overflows at 390 and 320px (section 25).

### 4.1 Tab title, search and share preview (the page head)

Sean asked for this on Oct 31: "the preview. When you send this link on Slack or something, there should be a good
preview image both for square and for landscape, like 16:9. We need a really nice image for that."
- **Tab title:** event name · what it is · with whom · dates, sentence case. Ana: "The Exit Plan · a free 3-day live
  event with Ana Calin · Dec 8 to 10". The VIP page: "VIP · The Exit Plan with Ana Calin".
- **Description** (`meta name="description"` and `og:description`): the hero promise in the host's words plus the
  format, dates and anchor time. Ana: "My newsletter business has made $1.4M. Here's what I'd do first if I wanted to
  leave my job in 2027. Three free live sessions with Ana Calin, Dec 8 to 10, 12:00 pm New York."
- **Share picture:** `og:image` as a full `https://` address on the live domain, `twitter:card` set to
  `summary_large_image`. Make two pictures in the client's art style with the event name, "free" and the dates: 16:9
  (1200 x 630) for Slack, LinkedIn and X, and a square (1200 x 1200) for apps that crop square. Ana: only the
  landscape one exists (`img/share.jpg`, 1200 x 630). **Still to do:** the square picture, and a re-check of the
  picture after the date move (it must not show Nov 17 to 19).
- **Theme colour** = the page ground (Ana `#FFF8EE`), so the phone browser bar matches.
- **Favicons:** the host mascot set (`ui-kit.md` section 17): `favicon.ico` (16, 32, 48), a 32px PNG, a 192px PNG and
  the 180px `apple-touch-icon`, each link with a `?v=` hash so browsers fetch a changed icon.
- **Search engines:** every page carries `<meta name="robots" content="noindex,nofollow">` while it is built.
  **Still to do (launch day):** take noindex off the registration page only; the VIP, confirmation and tool pages stay
  noindex. Trial pages (`/v2/`) are always noindex.
- When a domain changes, change every absolute address in the head (`og:image`, calendar files, share links) in the
  same commit. Ana: the share picture first pointed at a Vercel address that did not resolve.

---

## 5. The hero (full detail)

### 5.1 Purpose

The first screen must do four things at once: show the host talking (the video), state the promise (headline),
name the event, the dates and that it's free, and put the form in reach. Sean on the video: "I want the video to be
seen right away, and then the form."

### 5.2 Desktop layout (1061px and wider)

- **Two columns.** Left: the video column. Right: the text and form column. Grid on Ana's page:
  `.v2h.hgrid{grid-template-columns:minmax(0,1.52fr) minmax(0,1fr)}` from 1061px (it started at about 1.44fr / 1fr
  and grew when the video window was made bigger); gap 40px; `.hwrap` max-width 1400px, padding 0 32px.
- **The video column is always the wider one.** Sean: "I want the column of the video to be bigger than the text
  column, just like before." Claude had narrowed it to 1.1fr / 1fr to fit a bigger headline; that was reversed.
- **No second column of text.** Two text columns side by side in the hero was rejected ("I don't like this idea about
  two-column text"); the left column is a graphic (the video), the right is the copy and form.
- **Never squeeze the headline above a narrow form.** A 368px and then a 292px headline-plus-form column were
  rejected as too small and plain. The right column is wide enough for a big headline.
- **Do not centre it, do not stack it.** On Nov 4 Sean first asked for the video under the headline on laptops, saw
  the centred build and stopped it: "Is it even a good idea to put it in the center? Shouldn't it be the same, where
  everything is on the right? It looks really weird, like everything under the video. Shouldn't we keep it the same
  layout, but thinner, of course?" Lesson: when the form is low on a laptop, tighten the approved layout first
  (section 5.6).
- **No experimental editorial hero.** A full-width bold editorial headline over a 1030px video was tried on Oct 31
  and dropped ("There's too much white space going on in the header headings.", "Isn't it that the video is a little too big here?",
  then back to the old layout).

### 5.3 Left column, top to bottom

1. **Trust strip** (`.tstrip`): the brand badge, then three bold numbers with short labels. Compact: about 58px tall,
   sized to its content (`width:max-content`) and centred over the video window, not stretched to the column (Sean
   found it bulky, then too long and empty).
   - Ana: badge "HOW WE GROW / with Ana Calin" (badge image 32px, small caps 8.5px), then "$1.4M from the newsletter",
     "About 80,000 readers", "0 sales calls" (numbers 16px bold, labels 9px caps); padding 6px 14px 6px 6px, radius 14px,
     margin-bottom 18px.
2. **The video, inside a scene from the client's world** (`#vsl.iph.win`). The video is big, framed by a painted
   object that opens on load.
   - Ana: her painted Greek window (`img/vip/paint/winh.webp`), two blue shutters that swing open in 3D on load, a few
     bougainvillea petals fall, the flower box is a separate smaller layer (`.wn-pot` scaled .74) so it covers less of
     the picture. Sean: "go ahead, use the shutter window." Window margins on desktop `11% 11% 11.5% 2.5%`.
   - The window gets breathing room above it: it must not touch the trust strip (shutter tops once touched it).
   - Cover: a still of her talking to camera (`img/vsl.webp`), a round play button with "tap for sound", a player bar
     with the time left (`-2:34`). The pill and bar hide while the video plays.
   - Video files: `VSL_SRC` and `VSL_SRC_P` in the page script (a landscape edit for the window, a portrait edit that
     opens full screen on phones). See `../video-editing.md`.
   - The window video loads nothing until it is tapped (`preload="none"`); a tap plays it with sound, a second tap
     pauses. On phones (640px and narrower) the portrait edit opens full screen in a lightbox; when it ends, the
     lightbox closes and the page scrolls the hero form to the middle of the screen, because the video ends on "put
     your name and email in the form". Ana: built Nov 4 on the work branch, live only once Sean says publish.
   - Remove crowding: Day 1/2/3 cards that once sat under the video were removed. Sean: "let's try to push down the
     slide with the CTA button and try to remove the day 1, day 2, day 3 here. Because I think there's just too much
     going on. They won't be able to breathe."
3. **Booking strip** (`.book`): a small slide thumbnail, "Free / live on Zoom", "Join The Exit Plan, free.", the dates,
   New York time plus one other city, and a button.
   - Ana: "Tue Dec 8 to Thu Dec 10", "12:00 pm New York / 7:00 pm Greece", button "I want my exit plan, free".
   - A visitor outside New York sees their own dates, then their time and city before New York (Ana `.book .d` and
     `.book .t`: "Wed Dec 9 to Fri Dec 11", "1:00 am in Manila / 12:00 pm New York"). Rules: [ui-kit.md](ui-kit.md)
     section 15.
   - Sean asked for it back after Claude removed it as a duplicate ("can you put this back"), then "less bulky, more
     compact". No extra small text crammed in (the "3 days live" line was removed).
   - Keep the same small gap under the hero art at every desktop width (tie the gap to the art's size): Ana
     `.v2h .hleft > .book{margin-top:calc(13.7% + 34px)}`, checked at 1100, 1280, 1440 and 1920.
   - 1061 to 1340px: the button goes on its own row under a dashed line (`grid-column:1 / -1`), full width.
   - Below 1061px the strip hides; the phone bar replaces it.
   - Its button opens the sign-up popup, like every button (section 20).
4. **Hero notes** (`.hnote`): one plain reassurance line, then two bold-lead lines for edge audiences.
   - Ana: "You don't need a newsletter, an audience or an idea ready." / "**Already self-employed?** Your goal might be
     to earn without taking on another client. Bring that goal." / "**Been to one of my workshops before?** I'll show
     you which parts of my business I'd build first today, what I'd move earlier, and why."

### 5.4 Right column, top to bottom

One clear order, obvious hierarchy. Sean on a version with copy everywhere: "The text placements are very wrong. They
don't have hierarchy. Everything's all over the place."

1. **Pill** (`.hpill`): event name, free, length, where; the secondary words not bold. Visible on laptops too (it was
   hidden on short screens for a few minutes on Nov 4, then brought back).
   - Ana: "The Exit Plan · Free 3-day event live on Zoom", with "live on Zoom" at weight 500; a pink live dot.
2. **Headline** (`h1#h1.h1x`): a small pre-headline line with the proof number highlighted, then the promise in
   hand-set whole-phrase lines, the year in the accent italic.
   - Ana: `.h1a` "My Newsletter Business Has Made $1.4M." at .46em, `$1.4M` in `.hl` (solid sunflower highlight), then
     "Here's What I'd Do First / If I Wanted to Leave / My Job *in 2027*." (`.h1b .l` lines, `white-space:nowrap`,
     "in 2027" `em` pink italic).
   - Size: as big as its column allows, the loudest thing on the first screen, but never so big it fills the page
     width or leaves white gaps, and never running under the frozen form. Ana: `font-size:min(13.4cqi,84px)`, line-height
     1 (about 69px at 1440). Phones: `min(14.2vw,60px)` (about 55px at 390), five whole-phrase lines (`.h1b .m`
     forced to their own line).
   - Sean: "i said you can make this bigger". When he says "make the header bigger", confirm which heading: once it
     meant the page H1 and Claude enlarged the form heading by mistake ("Wait, I meant the heading of the page...").
   - Size the headline to its real text width (measure the text, `width:fit-content`), not the box, so no empty space
     sits beside it. Sean: "There's too much white space going on in the header headings."
   - Headline pattern for any client: first person, the host's proof number, then what she'd do first, then the target
     year. Ana's earlier headlines ("How to Build the Income That Lets You Leave Your Job in 2027", then "How to Build
     the Business That Pays You for What You Know in 2027") were replaced by her Nov 3 copy. When Sean offers a choice
     of words ("income or business?, which is better"), pick the concrete one and say why.
3. **Bold promise line** (`.hlead`): names the three things they will learn, in the sans.
   - Ana: "I'll show you what I'd sell first, why someone would pay for it when advice is everywhere, and where I'd find
     my first customers."
   - The line under a hero H1 is always sans, never the display serif (Sean: "use sans serif").
4. **One short paragraph** (`.hsub2`): the format and the twist, numerals in brackets.
   - Ana: "Join me for **three (3) free, live sessions** to see what AI has changed about the order I'd follow, and
     work out where you could begin with the experience you already have."
5. **One highlighted reassurance line** (`mark.sk`).
   - Ana: "You can start alongside the work that pays your bills."
   - Keep 4 and 5 ABOVE the form. Claude moved them under the form to lift it; Sean: "Even this one, the text
     underneath the form is still weird." They went back above.
6. **The form ticket** (`.htk .tkt#hcard`): proof bar on top, inside the card, separated by a thin line; then the
   eyebrow, the heading, the fields, the button. Full spec in [ui-kit.md](ui-kit.md).
   - Proof bar: five student faces, five stars, "800+ student wins" until the real registrant count passes 50
     (section 22). Sean: "Can you make the form narrower and put the testimonial bar on the top".
   - Eyebrow: "Free · 3 days live · Dec 8 to 10"; the visitor's own dates and city lead it when they differ, set
     bigger than the rest of the row (Sean: "make date bigger here"; Ana `.r1 b` at `1.32em`).
   - Heading "Save your free seat" on one line (36px Manrope 800, `nowrap`), then in the serif "Join me for all 3 days
     (for free)." (Sean: "Join me for all 3 days and add for free (inside parentheses).")
   - Fields with visible labels "First name" and "Email", button "I'm in, Ana (it's free)", ticks "Free / 3 days live
     with me / Come as you are", meta "12:00 pm New York · About 90 minutes a session", and the email note.

### 5.5 Desktop and laptop: what is on the first screen

Checked sizes: 1280x720, 1280x800, 1366x768, 1440x900, 1536x864, 1680x1050, 1920x1080.
- The video top left is fully in view on every size.
- The headline, the promise line and most of the form are in view. The button may sit slightly below the fold on
  short laptops, accepted because the floating header button is always in view. Ana's measured gap to the button:
  about 110px at 1280x720 and 1366x768, about 75px at 1440x900, fits at 1920x1080.

### 5.6 Laptop fit rules (in this order)

When the form or button falls below the first screen on laptops:
1. Tighten the approved layout first: thinner right column, smaller gaps, a compact form card.
2. Then shrink the headline a little, only on short screens.
3. Never move the supporting copy under the form, never centre the hero, never stack it.

Ana's values (`@media (min-width:1061px)`):
- Right column as a flex column; promise line margin-top 14px; ticket `order:5`, margin-top 16px.
- `max-height:930px`: H1 margin-top 10px, ticket padding 12px top and bottom, heading 31px, its second line 19px,
  fields 48px tall, button 54px.
- `max-height:830px` (1366x768, 1280x720): H1 `min(9.4cqi,56px)`, promise line 17px. At 900px tall (1440x900) the
  headline stays full size.
- `max-height:760px`: H1 `min(8.8cqi,50px)`, promise line 16.5px, heading 29px, fields 46px.

### 5.7 Big monitors

- From 1800px wide the whole page is enlarged evenly with CSS `zoom`, by the screen's width and height so the hero
  still fits, up to 2x: `k = min(w/1600, h/1075, 2)`, ignored under 1.05. Lengths tied to the screen (100vw, 100vh)
  are divided by `--z`. The script sits in the `<head>` before any CSS.
- 1440 to 1920 stays as it is. Never scale laptops up: it pushes the form down.
- Claude's judgement Sean agreed with: "Big monitors (around 1920 and up): yes ... Laptops: don't scale up. It would
  hurt sign-ups." Sean: "Yeah, I think we can scale for big monitors, for sure."
- **Still to do:** tested in Chrome only; Safari handles `zoom` differently. Check on a Safari big screen.

### 5.8 The frozen side form (1280px and wider)

- Once the hero's ticket scrolls away, the same form moves into a slim column frozen on the right (`aside.v2rail`),
  centred on screen under the floating bar: `top:max(92px, calc((100vh / var(--z,1) + 74px - var(--tkh,480px)) / 2))`.
- Width 284px (`--rw`), 44px gap to the page content (`--rg`); the page content keeps its margin on the right so
  nothing runs under it.
- It appears only after the form has moved into it, so two tickets are never on screen with one empty; it arrives in
  .18s. The hero ticket keeps its height while the form is away, so the page never jumps.
- Typing in one ticket never makes the form jump; the form always returns to the ticket on screen.
- Below 1280px there is no rail; the buttons and the popup do the job.
- Where it came from: Sean, Oct 31: "I want to freeze the form on the right side ... I want to stick with the two-column
  layout ... Since Anna's form is simpler, we can make it thinner, slimmer, so there's more surface area for the page
  content itself." It was built as a trial at `/v2/` (noindex) with the live page untouched, then became the main page.
  The sign-up column was tried at 292px and the ticket at 256px; the rail settled at 284px.
- A half-and-half cookie split (`ana_sticky` on/off) is sent with the sign-up as `sticky_variant`, to measure it.

### 5.9 Motion in the hero

- Shutters swing open on load, finishing well under 2s; petals fall; the play button ring pulses softly (transform
  and opacity only).
- The ticket sways a little every 7s, the next empty field glows, then the button once both are filled; all of it
  stops while someone types, none with reduced motion. Never a strong pulse on a field (`../motion.md` §1).
- Stats and badges never pop for attention.

### 5.10 How it adapts to another client

- Video frame: a painted object from the client's world that opens (a door, a window, a curtain, a shop shutter), not
  a phone mock or a plain rectangle. Painted tight so the video stays big.
- Trust strip: their brand mark plus their three strongest true numbers.
- Headline: their own proof number in the pre-line, their promise, their year or deadline in the accent.
- Highlighter: their accent, used the same way in the video and graphics so they match.
- Edge-audience notes: the two groups most likely to think the event is not for them.

### 5.11 Score and open issues

- Score: 9/10 on desktop and laptop (approved layout, measured fold, fast). Points off: button below the fold on
  short laptops by design.
- **Still to do:** the Safari big-screen check; tablets and phones (section 25).

---

## 6. Opening section: "You want to know..."

- **Purpose:** the reader sees their own situation, then meets the host as a person (face first).
- **Layout (desktop):** a centred two-line serif statement across the top, then a grid of the host photo
  (narrow, top-aligned) and the text, then the CTA with a "when" line beside it. Ana: `.intro.who{padding:120px 0
  116px}`, `.who .iq` `clamp(34px,3.7vw,54px)`, margin-bottom 76px; `.who .igrid` `minmax(0,.5fr) minmax(0,1fr)`, gap
  `clamp(40px,5vw,80px)`, max-width 960px; photo max-width 300px.
- **Type:** first line `clamp(25px,2.2vw,31px)` with its key phrase bold on a highlighter band; paragraphs 18px,
  line-height 1.72, 18px apart; the key sentence in `mark.sk`, weight 600.
- **Breathing room, never cuts.** Sean: "I don't want to remove anything. I just need to be able to breathe because
  there's a lot of text." Add space and shorten the line length; keep type at reading size. A first pass shrank the
  text (46/27/16.5/14px) and Sean asked "Isn't the text size a little bit too small?"; sizes went back up, the spacing
  stayed.
- **The host's face is required** in any section where she speaks in the first person. Sean: "Where is Anna's picture
  here? Also, this section looks very repetitive. There's too much text going on." Fix repetition with a better layout,
  not only trimming.
- **Photo frame:** a painted picture frame in the house technique, not a flat rectangle ("should we make this a
  picture frame in our graphic techniques instead. not a rectangle yelllow and white"). Leave room in the art canvas
  for its shadow. Ana: `figure.pframe` with `img/vip/paint/ana-frame.webp` (960x1360), photo `img/real/ana-studio.webp`.
- **Signature under the photo** (signature rules in [ui-kit.md](ui-kit.md) and `../motion.md` §3): a real, readable
  signature traced from a script font (Ana: Meddon), written by a nib in about a second, in the page accent (Ana
  `#F72585`, deeper while wet). The client's real wordmark sits beside it on the same line, small, aligned to its
  middle, with a thin divider, never under it ("looksbad, put it on side instad"). Centred on the mat, not hanging
  low ("signature should be pushed up a bit so its balanced").
- **Partner line:** when the visitor comes from a partner newsletter (`?ref=` matched in `partners.json`), a bold
  line above the heading names them, followed by "sent you here. Here's who I am." Hidden otherwise.
- **Ana's copy:** "You want to know / *you could make it on your own.*" Then "You can be very good at your job and still
  wonder **what anyone would buy from you directly.**" ... "I want you to start finding out what your experience could
  earn while your current work still pays the bills." Button "I want my exit plan, free", beside it "Dec 8 to 10 ·
  12:00 pm New York / Free and live on Zoom" (`.iwhen`). A visitor elsewhere sees their own dates, time and city on
  the bold first line ("Dec 9 to 11 · 1:00 am in Manila"), then "Free and live on Zoom".
- **Score:** 8/10. **Superseded:** on Nov 2 a sunflower sat behind her photo; on Nov 3 the painted picture frame
  replaced the photo's flat yellow-and-white rectangle and there is no sunflower behind it now. If a brand graphic goes
  behind a host photo, it shows around the frame and never reaches into the text.

---

## 7. The three days

### 7.1 Purpose and order

Show the mechanism: three named steps, each with what you leave with, building to the next. Head, slide wall, a
sticky progress tracker, one row per day, then "come to all three" and the featured result.

### 7.2 Head and slide wall

- Two-line serif heading, then one lede with its key phrase highlighted. Ana: "Here's what we'll work / *through
  together.*" and "I'll show you where I'd begin, the decisions I'd make before building more, and what taking this
  further could look like."
- **Slide wall** (`.swall`): a strip of the event's real slides staggered in on scroll, labelled "From my slides for
  the three days", the second row cut off (an open loop; Fladlien). The same slides play in the day windows, the recap
  and the booking strip.

### 7.3 The progress tracker

- A slim Day 1 to 3 tracker stays on screen while reading the days: current day big and in the accent, finished days
  ticked and small, the next faded (Fladlien's mechanism-with-progress).
- Desktop: top right (`.dmap{justify-content:flex-end;top:96px}`), Sean: "can you put this floating thing for days 1
  to 3 under the top-right side instead". Phones: smaller, `top:8px`.
- Its labels match the day titles and the recap exactly (Fladlien: show the plan three times): Ana "Your people / What to sell /
  The path".

### 7.4 One row per day (desktop 1061px and wider)

- The date, the headline and the first paragraph run full width across both columns; the slides window sits beside
  the bullets and stays in view (sticky, top 170px) while they scroll. Rows alternate sides (`.drow.flip`). Sean:
  "You can probably widen some text on the top here since there's still a lot of space on the right."
- 1060px and narrower: stacked.

### 7.5 The day pattern (copy)

Every day block:
1. Small label: day number, weekday, date, time (the visitor's own date, time and city when it differs, New York in
   grey beside it: `.dny` 13.5px, weight 600). Ana: "DAY 1", "Tuesday, Dec 8", "12:00 pm New York".
2. Headline with a subtle highlight on the key phrases only (`.dh`: a 42% sunflower band from 58% to 90% of the line,
   lighter than the main highlighter). Ana Day 1 "Find the **people your business could serve**."; Day 2 "Find the
   **part of what you know** that **could become your business**."; Day 3 "See the path from your first customers to
   a business of your own."
3. A bold lede line. Ana Day 1: "Where I'd find my first audience if nobody knew my name."
4. Two or three short body lines, one key phrase in `mark.sk`.
5. Three to five bullets, each starting with a bold lead sentence. The bold lead never breaks into one word per line.
6. An outcome label: "You'll leave knowing" / "You'll leave with" / "Come with".
7. A bridge line to the next day. Ana: "Then comes the question that makes Day 2 matter: **what could you sell that
   makes this worth building?**"
8. Its own CTA: "Show me where to start (it's free)", "Help me choose what to sell (it's free)", "Show me the path
   (it's free)", each with "free · live on Zoom" under it.

### 7.6 The day windows (slides)

- Each day window plays two real-looking slides of that day as a live screen share when scrolled to: a "LIVE Day 1 ·
  Ana is sharing her slides" bar, the host's camera tile lit while she talks (face framed whole), the day's second
  slide fanned behind. Slide area fixed at 16:9 so it never collapses.
- Slides are teasers, not title slides: built to intrigue, the method covered by black bars and lock stickers so
  nothing is invented. Only readable words from the registration copy; dashboards, emails and posts are labelled
  mock-ups; a lock label like "Shown live on Day 1" (and, in the first teaser set, a page number like 14 / 52
  so it feels like a real deck); no event dates on the slides. Sean: "I want
  to put the real slides, real-ish, something built to intrigue people, secret sauce."
- Balanced inside: text not too low, the graphic not pushed to one side, cards fitting their headline. Sean: "I love
  the slides, but the placements in it are not balanced."
- Each day's sky says its time of day (Ana: sunrise, midday, sunset over the sea).
- Follows the factory's slide guideline and [fladlien-on-pages.md](fladlien-on-pages.md).

### 7.7 "Come to all three" and the featured result

- A short bold line with its own button. Ana: "Come to all three (3). Give yourself time to work through the decisions
  and see how they fit your situation." Button "I'm in for all three (free)".
- Right after it, one featured student result in her own words (Ana: Jill Hart's Substack note, "I was able to
  monetize a 300ish audience and make over $3K in a month." with "From Jill's experience working with Ana. Individual
  results vary."), then the results trio (section 8).
- **Score:** 9/10. **Still to do:** Sean planned animated scenes per day (dashboard ticking up, blacked-out words, 771
  vs 82 likes); the slides shipped instead.

---

## 8. Results trio

- **Lead with the strongest concrete results** (money or growth from small lists), as big figures, labelled clearly
  as coming from a past program. Sean: "Can you choose better testimonials with better results than these?" and
  later "Why are those small list testimonials different? Where's the 3,000+, 3,200, 2,400? Also, make the text maker
  show us that these are from the past challenge."
- Never swap a headline result for a weaker one because the weaker one has a screenshot. Never remove the side cards
  in a redesign ("dont remove the other 2 testimonials here").
- Real screenshots where they exist; when the screenshot is missing, rebuild the person's note word for word as text
  (a Substack note card) and ask the client for the image. Never drawn mockups as proof.
- Each card keeps its original wording, a counting-cash animation (notes land on a pile while the amount counts up),
  and a small "Results vary" line; the block ends with a disclaimer naming the source.
- Never use results that are unverified, anonymous without the client's OK, told two different ways, or named only by
  first name and initial; flag them. (Ana's 312-subscriber story was left out as conflicting.)
- Ana: "$3,000+ in a month, from about 300 readers" (Jill's note), "$3,200 from 547 subscribers" ("First launch ever.
  Three emails, launched the same week."), "$2,400 from 198 subscribers" ("She almost didn't start because she thought
  198 subscribers wasn't enough. It was."), then "Individual experiences from my past challenge. Results vary."
- **Open:** the $3,200 and $2,400 students are anonymous; flagged for Ana to confirm.

---

## 9. Situation picker: "Where are you right now?"

- **Purpose:** the visitor picks who they are; the pick personalises the button and is sent with the sign-up.
- **Layout:** eyebrow, a two-line heading, three illustrated choice cards in a row, one centred button below with a
  small line. Cards stack on phones.
- **Cards:** each a painted scene built around the event's core idea, reacting to the pick (not flat icons): on hover
  the scene starts to move; when picked the card fills with the accent, gets a check, the scene finishes its move,
  and the button text changes. Card labels never inherit heading styles and never wrap. Sean: "Better concept for
  that section."
- **Background:** a metaphor that reads at a glance. Ana: three roads, one from each card, meeting at the button
  where the plan rises like the sun; roads hidden on phones. (Faint lines that didn't read were replaced.) Ground
  `--sand:#FFF1C9` with a soft yellow glow.
- **Ana's copy:** eyebrow "Where are you right now?", heading "What would you like *to change about work?*", cards
  "I have a job. I want leaving to become a choice I can afford." / "I work for myself. I want more income without
  filling every available hour with client work." / "A bit of both. I want to choose one business direction instead of
  squeezing more work around everything else." Button default "I want the plan", job "I want out by 2027!", self
  "I want to get paid for what I know", both "I want the plan"; small "free · live on Zoom". Hidden field
  `fields[situation]` = job / self / both.
- **Score:** 8/10.

---

## 10. Host story

- **Purpose:** why her, told as a story with one honest failure, her real numbers, and what she'll do for you.
- **Layout:** text left, a photo stack right: a square photo, her own painting as a die-cut sticker, and a "then and
  now" card that looks like a raw platform screenshot.
- **Headline:** the failure as the hook. Ana: "I'm Ana. / *My first workshop sold two (2) copies.*"
- **Scannable story:** break it into short lines with a creative bullet from the brand mark beside each heading line
  (Ana: painted sunflower petals, each a different shape, size and angle), only on heading lines, large enough to read.
  Sean: "You can probably make the bullet a bit more creative, maybe like one of the petals of the sunflower logo."
- **Proof card:** a compact replica of a real dashboard (Ana: a Google Ads-style "Overview / All time" with First
  sales 2, Readers 80K, Revenue $1.4M, Sales calls 0, a line rising from "First workshop" to "Today"), with no
  hand-drawn marks over UI-style pieces and no cut labels. Sean: "I want that to look a little bit more like a raw
  screenshot instead of something like this. It looks Claude-generated if we keep it like that." Use the client's real
  screenshot when she sends it.
- **People she has learned from** (social proof from collaborations, Ana Nov 4, `.convos` at the end of `#host`,
  full width under the story and the photo stack). The rule for any client: show real frames from the host's own calls with known people, never links, play
  buttons or logos; one short credibility line per person, taken only from that person's own pages or own words.
  - **Why frames, not names or faces.** It started as small face circles under "I've recorded conversations on my
    Substack with". Sean: "i kinda wanna show these instead like the actual video frames" and "doesnt have to be on
    substack, just gotta tell ppl she got insights and had a convo from them too. make the design look more fit to the
    section and page". So no platform is named; the heading says what she got from them.
  - **Only people with a real frame.** Sean: "maybe not have to include kristina coz we don have vid of her". A guest
    without a real frame from the call is left out, never shown with a stand-in picture.
  - **No logos.** Sean: "we can add logos of their stuff". Claude declined: logos imply a partnership and clutter the
    row. One short credibility line under each name does the job instead (Sean: "yes add short line of credibility
    too").
  - **One iconic picture is fine.** Sean: "okok you can prob put this justin welsh pfp on his stuff coz its iconic".
    Ana: Justin Welsh's round profile photo as a badge on his print's bottom right corner (`img.cv-pfp`, 34% wide,
    white ring, ink edge, tilted 4deg). Only for a face people know at a glance.
  - **The best checked line, not the first one found.** Sean: "for micheal why read tens of millions of times" then
    "first. make sure all of em have the best bio here". Each line comes from the guest's own site or own words and is
    checked. Where sources disagree, the number goes (Mary: 725 vs 722 weddings, so no count). Pick wording that never
    breaks badly (Sean: "fix line"; Justin's line is two `nn` chunks, one line or a clean break).
  - **Ana's six** (all real call frames, `img/collab/live-*.webp`): Justin Welsh "built a $15M solo business" (his
    site says one-person business); Mary Bartnikowski "photographed the Dalai Lama"; Michael Simmons "published in
    TIME, Forbes and HBR"; Ciler Demiralp "analyzed 75,000 Substack newsletters"; Dr. Nicole Pertillar
    "board-certified health and wellness coach"; Marni Battista "Hay House author, coach for 16 years".
  - **Design: small prints like the host photo above,** so the row belongs to the section. Ana `.cv-ph`: white mat
    (6px), 1.5px ink edge, yellow offset shadow (`5px 5px 0 var(--sun)`), a strip of tape on top alternating pink and
    yellow, tilts in a repeating -2deg, 1.4deg, -0.8deg; frames 3:2. Names in bold sans (Sean: "use sans serif for their
    names"; Ana Manrope 800, `clamp(13px,1vw,14.5px)`, `nowrap`) with the green video-call icon before each (Sean: "and
    add a call graphic beside"; `#vcall`, the page's own icon, never FaceTime's). The credibility line in grey under it
    (12.5px, `--ink3`, balanced).
  - **Not clickable,** so nothing pulls people off the page. 6 across on desktop, 3 on tablets (1060px and below), 2
    on phones (640px and below).
  - Heading in the section's serif: "People I've sat down with, *and learned from.*" (`.cv-k`, the second half pink).
- **Footnote for every number claim:** Ana's footer: "$1.4M and reader count: my own figures, published on
  howwegrowtoday.com."
- CTA: "Show me your numbers, Ana (free)".
- **Open:** real screenshots of the 771-like and 82-like posts and the two-sale workshop's sales page were asked of
  Ana.

---

## 11. Why attend live (live review)

- **Purpose:** the reason to come live rather than wait: the host reviews real work on screen.
- **Layout:** the split pattern (3.2): eyebrow, heading and the question list beside a painted desk scene, then a
  dashed divider and the paragraphs in two columns, then the button.
- **Heading:** a five-line heading is split into a main line and a smaller sub-line. Ana: `h2.bring-h`
  `clamp(34px,3.4vw,50px)` "Bring your business idea." with `.l2` in bold pink sans (`clamp(18px,1.45vw,21px)`, weight
  700, max 26ch): "I'll review selected ideas live and show you what I'd change."
- **Question list in sans**, 19px, weight 700: "What if I have two completely different ideas?" / "What if people
  already get this advice for free?" / "What if I can only work on it after my job?", then "Bring those questions."
- **Scene:** laptop with the real compose screen, coffee with steam, a sheet the pencil edits by hand ("Say the price
  in / the first line."), and a question bubble "Is my opening line clear enough? / Ana is answering this live". Hand
  marks never cut off. Background: her editing marks at the edges.
- **Honest limits in the copy:** "I'll review selected attendees' work on screen", never "everyone's".
- Sean on spacing here: "spacing looks unbalanced and too scattered"; fixed with even, compact gaps.
- CTA "I'll bring mine (it's free)". **Score:** 8/10.

---

## 12. The gift (calculator)

- **Purpose:** a reason to sign up now; the tool unlocks after registering.
- **Copy rules:** say plainly what it is (a calculator). Describe it by what it shows the person (their own numbers),
  never as a promise; promise only what the tool does today. Tie it to a day. End with an estimates disclaimer.
  Sean: "Also, in the copy, can you say that this is like a calculator, so they would know they would get a
  calculator soon?"
- **Layout:** the split pattern: eyebrow, heading and the first two lines beside the laptop; four paragraphs and the
  note in two columns below; then the button. A "Free gift" badge sits beside the eyebrow and heading, labelling what
  it's next to (`../graphics.md` §5).
- **Scene:** the real tool's screens on a painted laptop on a textured, angled painted table (not flat): zoom into one
  real card, circle the key number, settle on the plan line; locked steps frosted under a band "The full calculator
  opens after you register"; an arrow to a postcard of the life the number buys with a "$3,000 a month" tag whose
  writing scales with the tag (`.gp-tag{container-type:inline-size}`). The tool's own logo badge sits in the scene.
  Sean: "cant see calculator" until the zoom made it readable.
- **Background glow behind the picture only,** fading to the pale ground behind text. Sean: "The gradient behind it is
  a little too dark. Maybe you can place it somewhere better that won't affect the text readability."
- **Ana's copy:** eyebrow "Your gift: the exit number"; heading "How many sales would you need / *to reach your monthly
  income goal?*"; "After you register, answer seven (7) quick questions to get your exit-number calculator."
  (highlighted); "**Bring those numbers to Day 2.**"; note "Planning estimates based on the figures you enter."; button
  "Save my seat and get my number" with "your exit number comes after you register".
- **Score:** 8/10. **Open:** Sean still wants the calculator itself tested ("We have to fix the calculators at the
  top and put the right stuff in it").

---

## 13. Fit check: "Wherever you're starting, bring that."

- **Purpose:** answer real objections as the visitor's own words, each with a one-line answer.
- **Form:** one notebook page: taped sheet, accent margin line, ruled lines, tick circles on the margin line; ticking
  tints the line and highlights the answer (Ana `.fit .fix span`, a 42% sunflower band 34% high); the button appears
  only after the first tap, centred below. Sean on a road behind the cards: "this execution looks weird".
- Never repeat the background device of the section above, and never run it behind cards that cut it.
- **Ana's copy:** eyebrow "Is this for you?", heading "Wherever you're starting, bring that.", "Tap the ones that sound
  like you." Five quotes, for example "I know my subject. I don't know what anyone would buy from me." / "Day 2 is
  where we look at what someone could pay you to help them do." After the first tap: "That's me. I'm in." with "Free ·
  3 days live".
- **Score:** 9/10.

---

## 14. Reviews and wins

- **Signal the section** with five small hand-painted stars that drop in above the heading, each slightly different;
  the testimonials eyebrow fills like a rating. Sean: "can you animate and draw something like 5 stars on top, just
  small 5 stars, just so they know what the section is for?"
- **Order:** a featured student story in her own words, then the review gallery, then the wins wall.
- **The featured story** (Ana Nov 4, `.jill.mrn` at the top of `#reviews`): the student's own words from a live
  recording, a real frame of that live beside them, and a label that says where it was said. Use only what the
  transcript says; a stronger claim from a post title or a summary stays out. Ana: Marni Battista, "I went from 25
  people on the wait list to 61 people on the wait list. Pretty much in two days." and, a week later, "I already paid
  for my investment."; byline "Marni Battista · coach for 16 years, Unscripted on Substack"; label "From Marni's
  experience in my bootcamp, said live with me. Individual results vary."; the frame `img/wins/marni-live.webp`
  tilted -1.2deg with the caption "Live on Substack with Marni". The post title's "5x her investment in 7 days" was
  left out because the transcript does not say it.
- **Gallery:** verbatim reviews (original wording, typos kept) in one card style, CSS-columns masonry (`.rgrid2{columns:3
  280px;column-gap:22px}`). Cards never split across columns (`break-inside:avoid`), or the card shadow shows as a
  stray black line at the top of the next column (Sean flagged it). Check at 720, 900, 1024, 1180, 1440px.
- **Wins wall:** raw screenshots of students' posts and messages on a pinboard; text cards with initials only until the
  real screenshot arrives (ask for it).
- **Phones:** 2 review cards plus "show all reviews"; the first wins plus "show all 9 wins".
- Ana's heading "Here's what students say about learning with me." / "These are their words, from previous workshops
  and programs."; disclaimer "Individual experiences from my earlier teaching and challenge. Results vary."; CTA "I want
  to see the work (it's free)".
- **Score:** 8/10.

---

## 15. Prize draw

- **Copy:** what is won, who can win, how (random), when, that it's free, that you must stay live. No value the
  current copy does not state (Ana's old "worth $3,000" was dropped).
- **Headline:** bold, not italic; the count as word plus numeral; the prize on its own line as a loud tilted label in
  a contrast colour that pops in on scroll; the key phrase never splits (check 320px). If the display serif has no
  bold, set the bold part in the page's bold sans. Sean: "make 1:1 and session in the same line. also make it diff
  color or som. make it stand out like rly stand out". Ana: "Five (5) people will win" then "a 1:1 session with me."
  with `.pz-hl` pink, white bold text, 2px ink border, `4px 4px 0` ink shadow, rotated -2.5deg.
- **Graphic:** make the prize tangible: Ana's video call rings, is accepted and opens on her face with your tile in
  the corner, beside five fanned 1:1 tickets (the top one with "your name?" written in, a round stamp "DRAWN LIVE · END OF DAY 3"). The
  phone never covers the ticket text. Use an original call icon, never Apple's FaceTime icon (`../SOP.md` E). Sean:
  "For the one-on-one with Anna, I was thinking of adding something into this, like Anna calling you one-on-one."
- **Ana's copy:** "Bring the idea you're considering, the decision you're stuck on, or the question you'd like more
  time to discuss." ... "I'll draw five names at random from the people still attending live at the end of Day 3." /
  "**Free to enter.** Stay until the end to be included in the draw." Button "Save my seat for the draw (free)".
- **Score:** 9/10.

---

## 16. FAQ

- **Layout:** the heading column stays in view (sticky) while answers scroll, with its own button; on phones the
  button comes after the questions.
- **Answers are honest and plain:** free means never having to buy; the paid upgrade is named as optional; no promise
  of outcomes; limits stated. No decorative bold "No." or "Yes." at the start.
- **Ana's questions:** Is it really free? / Do I need an audience or something ready to sell? / Is this only about
  newsletters or Substack? / What will I have by the end? / I've attended one of your workshops before. Should I come
  again? / How much time do I need? (about 90 minutes a session; prep tasks about 15 minutes each) / What if my subject
  has nothing to do with business? / Will you review my idea personally? / Will I be able to leave my job in 2027?
  ("I can't promise a leaving date.") Heading "A few things you might be wondering."; button "Questions answered. I'm
  in (free)".

---

## 17. Recap (closing ask)

- One big question, two or three short lines, the three day labels exactly as in the tracker, the event line, one
  button. Ana: "What could you build alongside the work you do now?" ... "Day 1 · your people / Day 2 · what to sell /
  Day 3 · the path", "The Exit Plan · Dec 8 to 10 / Three live sessions · About 90 minutes each · Free on Zoom", button
  "Yes, I'm coming, free".
- The event line follows the visitor (`.askt`): their dates, and their time and city added to the second line. Ana in
  Manila: "The Exit Plan · Dec 9 to 11 / Three live sessions · 1:00 am in Manila · About 90 minutes each · Free on
  Zoom".

---

## 18. Final invitation: "See you live."

- **Layout:** the host photo left in a simple device frame (Ana: a current iPad, thin even black border, camera in the
  top band, tilted 2.5deg; Sean found the first frame's borders too thick and dated), shown at its own proportions (no
  side crop), a calendar invite overlapping it, then date tiles, the heading, two lines, the session times with pins,
  the button and a small "Free · Live on Zoom".
- **The photo is the client's real one** (Nov 4). Ana asked to remove the AI First Class photo: "awful ... use one of
  the pics I gave you or a screenshot from my recording". It became a still from her own recording, then the real
  First Class photo Sean sent (`img/real/ana-cabin-real.webp`).
- **The frame stays simple; no app chrome around a client photo.** Sean asked for an "iphone look"; a true-to-life
  iPhone with the Photos app open (status bar, Dynamic Island, iOS buttons) was rejected: "iphone ui doesnt look
  realistic", then "dont use real iphone though i like the old size". The earlier wide, tilted frame with a thin
  dark border came back at its old size.
- **The calendar invite** is an exact Google Calendar invite in the brand colours, a cursor answering "Yes". It sits
  where the photo is empty and never hides what Sean wants seen. Ana: over the top right of the photo (the window row,
  three windows max), ending just above the lamp; text column moved right; the brand mark bottom left. Sean: "i said
  top right", "push a bit more to the right and a bit up. i wanna see the light". Values: from 981px `.claim .gi
  {right:-36%; top:-18%; width:72%; rotate(3deg)}`; 981 to 1240px `right:-15%; top:-14%; width:62%`; 980px and below
  stacked under the photo. Check 1100px and smaller laptops so it isn't cut at the top.
- **Date tiles and the calendar invite follow the visitor** (Nov 4): the three tiles show their own dates and
  weekdays (Ana `.final .tiles`, Manila "9 Wed / 10 Thu / 11 Fri"), and the invite shows their date and time as their
  own calendar would (`.gi-t`).
- **Times (`.ftimes`):** with the zone unknown, all the anchor cities as before. Ana: "Tue Dec 8 to Thu Dec 10",
  "12:00 pm if you're in New York", "9:00 am if you're in Los Angeles", "5:00 pm if you're in London", "7:00 pm if
  you're in Greece". Once the zone is known, their city leads, big and highlighted on top, their dates on the date
  line with New York's dates beside (under on phones); the other cities stay, small and grey, on an "Also:" line, two
  per row. Sean: "how about add an area for those but make their city the highlighted bigger one" and "make it 2 per
  column instead". Pros and cons of keeping the other cities were discussed; Sean chose to keep them small. Details:
  [ui-kit.md](ui-kit.md) section 15. Button "See you live, Ana!".
- **Background:** cream with one yellow sunrise and soft rays only (pink with yellow rays clashed).
- **Score:** 9/10.

---

## 19. Footer

- The client's village or world along the top edge of the footer (moved there from the hero, where it felt
  overwhelming: "these can be moved maybe on the footer instead so it wont look overwhelming").
- The same finish as the matching VIP footer (Ana: yellow with the VIP page's grain, `img/vip/paint/tx-grain.webp`).
- The source line for every number claim and the privacy link.

---

## 20. Popup form and exit popup

- **Every button opens the sign-up popup** (Sean: "show the pop-up form when they click any of the CTA buttons"); the
  ticket it leaves keeps its height. Ana: popup headline "Save your *free seat.*", "Join me for all 3 days (for
  free).", proof line, fields, button "I'm in, Ana (it's free)", "See you there, Ana" with her photo; thanks state "Your
  seat is *saved.*" / "See you Tuesday, Dec 8." (their own weekday and date when they are elsewhere: "See you
  Wednesday, Dec 9."), then on to the VIP page with first name and email.
- **Still to do (judges, Nov 4):** the popup has no "For you" time line, and in time-zone mode its eyebrow turns all
  pink; the email typo check lets a mistyped address through on the same click ([ui-kit.md](ui-kit.md) sections 8
  and 9).
- **What the sign-up sends and where it goes** (hidden fields, the server, the sheet, the next page): [ui-kit.md](ui-kit.md)
  section 8.1.
- **Exit popup:** opens once a session when the mouse leaves near the top edge (within 24px) on desktop, or on a fast
  flick back up (more than 700px in under 0.5s) after reading at least 35% of the page on phones. Never in the first 12s, never after they signed up or
  started typing. Ana: "Don't go yet. *Your seat's still here.*" / "Put your name on it before you go. It's free."
  Test link `?exit=1`.
- Details: [ui-kit.md](ui-kit.md).

---

## 21. Buttons and CTAs (and the word "free")

- **Say free on every sign-up button**, so nobody forgets it's free: either in the label ("I want my exit plan,
  free", "Yes, I'm coming, free") or as a smaller "(it's free)" / "(free)" (Ana `small.bq`, .8em, weight 600, hidden on
  the phone bar under 390px), plus a small "free · live on Zoom" line under section buttons.
- **First person, specific to the section:** Ana's set: "Show me where to start (it's free)", "Help me choose what to
  sell (it's free)", "Show me the path (it's free)", "I'm in for all three (free)", "Show me your numbers, Ana (free)",
  "I'll bring mine (it's free)", "Save my seat and get my number", "That's me. I'm in.", "I want to see the work (it's
  free)", "Save my seat for the draw (free)", "Questions answered. I'm in (free)", "See you live, Ana!". Main: "I'm in,
  Ana (it's free)".
- Brand icon on the left that moves on hover (Ana: the sunflower spins; in December it wears a Santa hat, kept in the
  lighter layer: "keep the xmas sunflower on the buttons lol"). Never greyed
  out. Details in [ui-kit.md](ui-kit.md).

## 22. Live proof (tickers, counts, names)

- Names and counts come only from the real sign-up feed (Ana `/api/ana-feed` reading Kit). Names come from sign-ups in the last 3
  days only (first names only, the latest 8), and show only when there are some. The count replaces the fallback by itself at 50
  (`FEED_MIN = 50`); until then a true fallback ("800+ student wins"). Never a line that would read 0 at launch.
- Ana's live seat ticker: a thin line (30px) along the top edge of three sections (where, reviews, final), in each
  section's own colours: a small "live" dot, then real first names drifting past with tiny brand pennants between them
  (the default, `section > .tkb`). Sean liked the departures board (ticker B) first, then said "Just make it more
  simple and something that adjusts the look of the section." and "maybe thats a bit too much tickers". The ferry
  departures board with flip letters stays only as a preview (`?tk=b`). Hidden until there is real data.
- The other live signals (all from the same feed, hidden without it): the "Maya just saved a seat · 4 min ago" pill on
  the hero ticket, "Maya just joined" in the popup's proof line, and a small toast bottom left. Spec:
  [ui-kit.md](ui-kit.md) section 13.

## 23. Section backgrounds

- One background idea per section, tied to its meaning, not generic coloured shapes. Sean: "Not just colored shapes,
  but actually think of a unique background for that specific section." Backgrounds add fun without changing layout.
- Grounds come from the client's fresh palette tints (Ana: cream `#FFF8EE` as default, sunflower cream `#FFF1C9` for
  the picker). No muddy beige or grey ("im not a fan of this puke poop grey color they dont really go well"), no grey
  texture overlays.
- Ana's set: hero, her village and warm light on stucco; days, sunrise, midday, sunset; picker, three roads; host, the
  Aegean in a Greek arch; bring, editing marks; gift, sunset sea behind the laptop; wins, a pinboard; 1:1s, call waves;
  final, the sun rising behind her photo. Scalloped edges between "sand" sections.
- December only: a light seasonal layer that switches itself off (`../graphics.md` §7). Ana's final set after "less
  christmas stuff" (Nov 4): the Santa hat on every button's sunflower, fairy lights on the frozen form, the wreath over
  the video window, the footer village lights, holly on the Day 1 tile, snow in the last section only. Gone: the hat on
  Ana in the header and the hero snow. Spec: [motion-and-speed.md](motion-and-speed.md) section 9.

## 24. Photos of the host

- Real photos only, traced to her own sources; never generate her face. Gemini polish of a real still only, by Sean,
  from Claude's prompt, then a non-AI finishing pass (about -3% saturation, warm orange-red hues pulled about 11%,
  fine grain stronger in shadows, about 0.7 degree tilt and 2% crop, normal JPEG/WebP compression). Sean: "What the hell
  did you use for the photo finish pass? How did it look more like her? Yes, use this."
- A lifestyle photo (a place, a trip) must read as a real phone photo, not a render. Show it at its own proportions,
  no side crop. Best is the client's own photo. Superseded: Sean once asked for a generated First Class photo "as
  realistic, taken from iphone 17 as possible"; on Nov 4 Ana called it "awful ... use one of the pics I gave you or a
  screenshot from my recording", and her real photo replaced it.
- **Never ship an AI picture of the client that she has not approved.** When she objects, swap in her own photo or a
  still from her own recording at once.
- **Device frames around photos stay simple:** a thin dark border, a tilt, no app chrome (no status bar, no Photos app
  buttons). Sean: "iphone ui doesnt look realistic" and "dont use real iphone though i like the old size" (section 18).
- A replaced photo is swapped everywhere at once (polaroid, day webcam, 1:1 call) under a new filename.
- Full rules: `../graphics.md` §4 and [ui-kit.md](ui-kit.md).

## 25. Phones and tablets: still to do

Sean's plan (Nov 4): desktop and laptop first, then "fix the design on mobile and tablets, and then we are going to
optimize all of them for all devices ... whether it's Android or iPhone". Known issues:
- **Still to do:** the phone bottom bar shows the visitor's dates but not their time and city; add them. It also
  overflows at 390 and 320px (judges, Nov 4).
- **Still to do:** on a 320px phone the form heading "Save your free seat" runs past the edge (judges, Nov 4).
- **Still to do:** the day map covers text in the Day 2 row (judges, Nov 4).
- **Still to do:** a full graphics and layout pass on phones ("some stuff that looks weird on phone, like the
  graphics and the layout").
- **Still to do:** tablets, portrait and landscape, as separate layouts ("if it's portrait for the tablet or if it's
  landscape, you should also think of that").
- **Still to do:** Android and iPhone checks for speed and animation.
- Already set for phones: hero order headline, bold promise, highlighted lines, form, then the booking notes;
  the H1 in five whole-phrase lines; justified text off; review gallery cut to 2 plus a button; picker roads hidden;
  FAQ button after the questions; the frozen rail off below 1280px.

## 26. Open issues on Ana's page

- **Resolved:** "usesans srif here" (Oct 31, 11:56) was the line under the H1; commit c2dcbc7 set it in the sans
  (section 5.4, item 3).
- **Open:** confirmation and VIP pages may still carry claims the registration copy dropped (prize "worth $3,000",
  48-hour replays); check every later page when a claim changes ([vip-page.md](vip-page.md)).
- **Open:** anonymous $3,200 and $2,400 results waiting for Ana's OK; real proof screenshots asked of Ana.
- **Open:** the registration page has no state for once the event has started or ended (the VIP page has one,
  `body.is-closed`). Ask Sean what the page shows from Tue Dec 8, 12:00 pm New York (late join, closed, or the next
  event) before launch.
- **Still to do:** the square share picture and noindex off on launch day (section 4.1).
- **Still to do:** Safari check of big-monitor scaling; phones and tablets (section 25).
- **Still to do (judges, Nov 4):** the frozen side form breaks "About 90 minutes a session" across lines; the popup
  lacks the "For you" time line and its eyebrow turns all pink in time-zone mode; the popup email typo check lets a
  mistyped address through on the same click (section 20). Phone bar, 320px heading and day map: section 25.

## 27. Done checklist for a registration page

1. Every section answers a buyer question, in the copy doc's order; nothing left from older copy.
2. First screen measured at 1280x720, 1366x768, 1440x900, 1920x1080: video in view, headline, most of the form.
3. Every headline checked for line breaks at 320, 390, 1024, 1440 ([layout-type-spacing.md](layout-type-spacing.md)).
4. Every button says free, opens the popup, and the popup submits to the next page with first name and email.
5. No proof without a source; disclaimers under every results block; no counts before real data. Collaboration proof
   is real call frames only (no logos, links or play buttons), each credibility line found on the person's own pages
   (section 10); a featured quote says nothing the recording does not (section 14).
5b. Every date and time on the page follows the visitor: checked in a far zone (Asia/Manila), in the anchor zone and
   with an unknown zone; a search for every month name, weekday and "am"/"pm" finds no mention left fixed
   except the anchor (New York) shown beside theirs.
6. No sideways scroll at 320 to 1440; no page errors; fonts load; reduced motion shows final states.
7. Seasonal layer checked on and off.
7b. Page head checked (section 4.1): title, description, share picture loads from the live domain with the current
   dates, favicons with a fresh `?v=`, noindex state as intended.
8. Sean's corrections logged in `../feedback-log.md` and this file updated (`../SOP.md` D).

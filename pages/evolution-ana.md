# How Ana's pages got here: first version to final, and why

Purpose: the story of Ana Calin's registration page (`/`, live at https://exitplan.howwegrowtoday.com) and VIP page
(`/vip/`) from the first version to today (Nov 4, 2026), so the next client's pages skip the detours. Every step says
what changed and why, with Sean's words where he gave them. Each step ends in a rule that works for any client in their
own brand, then Ana's example.

Read with:
[registration-page.md](registration-page.md) (the page section by section),
[vip-page.md](vip-page.md),
[ui-kit.md](ui-kit.md) (header, forms, buttons, popups, badges),
[layout-type-spacing.md](layout-type-spacing.md),
[copy.md](copy.md),
[motion-and-speed.md](motion-and-speed.md),
[page-sop.md](page-sop.md) (how a page job runs),
[fladlien-on-pages.md](fladlien-on-pages.md).
Generic rules live in [../graphics.md](../graphics.md), [../motion.md](../motion.md), [../SOP.md](../SOP.md); Ana's facts
in [../clients/ana-calin.md](../clients/ana-calin.md); every dated correction in [../feedback-log.md](../feedback-log.md).
This file does not repeat their detail. It explains how each decision was reached.

How to read an entry: **date · what changed** · why (Sean's words in quotes) · → the rule for any client · *Ana:* the
example. Times are the commit times in the client repo (seeeadd/2026-ana-calin). Where Sean reversed something, the
latest final version wins; the reversal is told only when it teaches something.

---

## 1. The arc in one view

| when | phase | what came out of it |
|---|---|---|
| Oct 25 to 28 | The paid program's offer pages (`/program` long, `/join` short), built before the event pages | No "AI pattern" layouts; one brand accent everywhere (yellow); the sunflower on the button; never grey a button; outcome-led button words; a makeover keeps the liked parts |
| Oct 28 | Sean asks for everything in one file for the next client (a multi-speaker summit) | The idea of this playbook |
| Oct 30 | Pages move to Ana's own repo and domain; sign-ups go to Kit through the API | Each client lives in their own repo and Vercel project |
| Oct 31, 02:00 to 14:29 | Registration trial at `/v2/`: two columns, a frozen form, a dozen layout tries | The old hero layout wins; the form sits in the hero and then freezes on the right; the form becomes a minimal ticket. `/v2/` becomes `/` at 14:29 |
| Oct 31, afternoon | Confirmation pages, the survey, the calculator lock, the spam step | Step order by importance; realistic app demos; data saved per person |
| Nov 1, morning | Calculator rebuilt to a spec; VIP copy brought up to date; Day 1 to 3 teaser slides | Tools friendly for 30 to 40 year olds; facts must match across pages |
| Nov 1, 13:48 to 17:45 | VIP page redesign, nine rounds | "the most perfect VIP page we have ever built". It becomes the bar for every page |
| Nov 1, evening | Registration rebuilt in the VIP finish, rejected, restored, VIP techniques added on top | "You honestly kind of ruined it": improve on top, never strip |
| Nov 2 | Dates move to Dec 8 to 10; backgrounds per section; forms that feel "already in"; glass header with countdown; tickers; email checks; badges; Christmas | The page gets alive without getting louder |
| Nov 3 | Sean's Nov 3 copy; Ana's painting as a sticker; her signature; the painted frame; the final photo; the prize label; our own video-call icon | Detail work: every small piece is designed |
| Nov 4 | The visitor's own time and city everywhere; laptop fit; numerals; big monitors; speed | Time is shown for one person, not for "your time"; fast without removing anything |
| Nov 4, 11:03 to 13:28 | Ana's and Sean's afternoon notes: real call frames of the people she learned from; Marni's live story; every date follows the visitor; a lighter Christmas; her real First Class photo | Social proof is real frames and checked lines, never logos; every date mention adapts; client photos are her own, in simple frames |

---

## 2. Before the event pages: what the offer pages taught (Oct 25 to 28)

These rules were set on the paid program pages (`/program`, `/join`) and carried straight into the registration and VIP
pages.

- **Oct 25 · generic layouts rebuilt.** A "crossroads" built as three Dec 30 screens side by side was rejected: "this
  looks like an ai pattern landing page build". It became a three-lane December timeline with Christmas week shaded.
  A four-icon "Everything inside" grid became a product illustration beside a plain list.
  → No three-card rows of screens, no four-icon grids, no interchangeable card stacks. Each section's layout comes from
  the client's world and the one idea it carries.
- **Oct 25 · sections that looked alike.** "also this one. everything looks about the same". The quote block, Ana's
  letter and the closing became three different forms: a dark band with four big numbers, a letter on paper in another
  serif with a clipped photo, a November wall calendar crossing off days.
  → Neighbouring sections never share a visual treatment.
- **Oct 25 · video position.** "shouldnt the vsl be put a bit up under headline".
  → Order in a hero: headline, one sub line, video, button with its small line, then proof.
- **Oct 25 · clarity.** "i like the idea but isnt it too confusing especially for a 40 yr old".
  → A clever idea that needs decoding is rejected. Simplify until the point reads at a glance.
- **Oct 25 · ground colour.** "also make the grey bg a bit lightwe". → A very light warm ground, never a mid grey.
  *Ana then:* `--ground:#F3F0EB`. (Later replaced by her cream, see section 9.)
- **Oct 25 · draft feel.** "everything still needs a detailed refresh. still looks like a draft, well it is."
  → Every block carries a concrete, specific point. No fluff.
- **Oct 25 · accent colour.** "Can you make yellow more of the main color instead of pink?", then "switch both to
  yellow too".
  → The client's signature colour is the one accent on every page and inside every mock screen: buttons, price pin,
  highlighter marks, badges. Yellow takes dark text. Third-party things in examples keep their own colours.
  *Ana:* sunflower `#FFD400`, dark text on yellow buttons; pink `#F72585` became the second accent.
- **Oct 25 · the brand graphic on the button.** "add a custom graphic that is clever and fits Ana's branding on the
  left side of the CTA button, something really made for her brand. Make it premiumly animated as well." The first
  sunflower was redrawn by eye and rejected: "doesnt look like her flower". It was rebuilt by tracing her logo file.
  → Brand graphics are traced from the real logo, compared side by side, then animated. The button graphic sits on
  the left of the label. (Its final behaviour: section 5.)
- **Oct 25 · greyed buttons.** "dont grey out any button." Before doors opened, buttons had greyed out and the header
  button had stayed bright.
  → Buttons never grey out. Before a sale opens, a click shows a short note with the opening date.
- **Oct 25 · button wording.** "Join now" was weak; "Save my seat" was questioned on a paid page: "also why is it
  "save my seat"". → Button words say what the buyer gets or starts, in their voice. "Save my seat" belongs to the free
  registration page only.
- **Oct 25 to 27 · makeover vs revert.** Claude reverted `/join` to the reference layout. "I didn't tell you to revert
  it. I like some parts of the stuff that you built with her own unique branding, but I just told you to give it a
  makeover with a compact layout."
  → A makeover keeps the parts Sean liked and changes the rest. Revert only when he says "revert". (The same lesson
  came back on Nov 1, section 6.)
- **Oct 27 · density.** "too bulky". → Prefer compact layouts; tighten rather than add blocks.
- **Oct 28 · carrying it on.** "Everything that we talked about from the registration page, the finalized preferences,
  and anything that would be great information for Claude Code to create the same types of pages: put them in a
  file." → After each approved client, package every final preference into the playbook (this folder).

---

## 3. Header

### Registration page

- **Oct 31 · top bar copy.** The pinned bar carried the event name with "free 3-day live", dates and time with the
  time zone, and one free button. A countdown and a join count had been squeezed in earlier and were taken out.
  → One bar, three things: what it is (and that it's free), when, one button.
- **Nov 2, 02:36 to 04:15 · the icon.** "I also want you to use the favicon of the page, the cartoon Anna, on the sticky
  header on top." Then "Also, I said to zoom this in, right?" (the first crop only trimmed the edge, and the browser
  showed the cached old file).
  → The header icon is the page favicon (the client's mascot), cropped tight on the face, no white edge. A changed
  image gets a new file name so caches can't show the old one. *Ana:* `img/o/fav/header-ana.webp`.
- **Nov 2, 04:29 · countdown.** A countdown to Tue Dec 8, 12:00 pm New York went into the bar.
  - "i want the numbers to be clearer and sans serif" → bold sans digits, seconds on yellow.
  - "Can you put the label underneath? Stick more to the numbers, so there's no weird gap in between." → unit labels
    tight under the numbers.
  - "I think the countdown is a little bit too tight." → clear space between units.
  - "For this sticky header timer, I want you to put "days left" on top, or something better than that." → "Starting
    soon" above the numbers in the same chip, with a round pulsing pink dot (never clipped into a pill shape).
  → A countdown is a small, clear chip: label on top, bold sans numbers, labels tight under them, room between units.
- **Nov 2, 04:53 to 05:31 · slim on scroll.** "can I make the sticky bar a lot more narrow, thinner, and smaller once I
  scroll, more compact?" The slim bar went 840, 744, 648, 588 px wide, then "it's a little bit too small. Increase the
  height", then wider again for the countdown label.
  - "Don't remove for free." (Claude had dropped "(it's free)" to narrow the bar.)
  - "don't remove the free 3-day workshop on the sticky header".
  - "Also, make the dates bold." (the serif has no bold, so the date is set in bold sans.)
  → A slim bar shrinks by tightening, never by dropping the event line, the date or "free". Say when it has hit the
  narrowest it can go. It must stay readable (Ana: about 52 px tall, 40 px icon, 14 px bold date, 42 px button).
- **Nov 2, 04:57 · material.** A dark glass bar was rejected ("I'm not a fan of the color"), then "There's no depth.
  It's just like no-opacity black-gray bill."
  → Light frosted glass with real depth: translucent pane that blurs what is behind, faint brand tints, a bright top
  edge, two-layer shadow. Countdown chips are small white glass with the seconds chip in the accent.
- **Nov 3, 09:12 to 09:23 · the event line fits.** "1&3 might need to fix text both sticky header versions". The caps
  line wrapped; sentence case fixed most widths; then it cut mid-word at narrow widths.
  → The event line is sentence case on one line. When space runs out, a script measures it and drops whole phrases
  (the host's name first, then the descriptor). *Ana:* "The Exit Plan · A free 3-day live event with Ana Calin".
- **Nov 4, 01:40 to 03:09 · the visitor's own time.** Full story in section 12. Final: the visitor's dates, time and
  city lead as the one bold line with a soft highlight and a tiny pink map pin; New York sits under it, smaller and
  grey. New York visitors keep the old header and height.

### VIP page

- **Nov 1, 15:40 · calmer header.** Light paper glass, the three steps on one thin line, "Don't close this page" kept
  on top, condenses on scroll.
- **Nov 1, 16:08 · still "meh".** "Can you make it look a little bit nicer, because right now it looks a bit meh?" and
  "On the sticky header, you don't have to put "optional." "Want the VIP upgrade?" Come on."
  → A floating rounded glass pill, steps segmented with the active one as a white pill, no "optional" on the upsell
  step.
- **Nov 1, 16:14 to 16:46 · the pink strip.** First a thin pink strip above the header that scrolled away. Then: "No,
  I don't want the pink strip to scroll away."
  → On any page that follows registration, a thin pink keep-open strip lives inside the sticky header so it is always
  seen. *Ana:* "Don't close this page. Your registration isn't finished yet."
- **Nov 1, 16:46 · a buy button in the header** ("Add VIP $67", hidden on phones where the bottom bar has it).
- **Nov 1, 17:34 to 17:45 · whose face.** The sunflower logo became the VIP profile photo, then: "Not that favicon,
  the one I used for the VIP confirmation page." Then "make the VIP favicon the browser tab icon too."
  → An upsell page wears the VIP mark (Ana: the cartoon with the crown on the pink flower) in the header and the tab.
- **Nov 1, 17:34 · remind them of the free event.** "Ana Calin" became "Free 3-day live workshop" with a pink date
  chip. On phones: "Free live workshop / Dec 8 to 10", and the steps show numbers only so nothing overlaps.

→ General: see [ui-kit.md](ui-kit.md) sections 2 to 4 for the finished header spec.

---

## 4. Hero (registration page)

The hero changed more than anything else. The lesson: the first approved layout was right; the fixes were size,
order and what goes in it.

- **Oct 31, 02:00 · try a two-column page.** "I want to freeze the form on the right side... I want to stick with
  the two-column layout... Since Anna's form is simpler, we can make it thinner, slimmer, so there's more surface area
  for the page content itself." Trial at `/v2/` (noindex), the live page untouched. Big video left, slim headline and
  form column right (368 px, then 292 px).
- **Oct 31, 02:19 · the headline was squeezed.** "I said two columns: the video on the left, the headers on the
  right... If it's put at the top of the form, it's too small there, so we need to really make it bigger."
  → A headline is never squeezed above a narrow form.
- **Oct 31, 02:25 to 02:35 · too much text in the hero.** "The text placements are very wrong. They don't have
  hierarchy. Everything's all over the place." Then a bold editorial hero (headline in Bonny 700 across the width,
  about 100 px): "There's too much white space going on in the header headings.", "Isn't it that the video is a little too big here?",
  "making the heading a little smaller? It's too big".
  → One reading order: small pill, big headline, one sub line, then the form (or one short paragraph). Size the
  headline to its real text width, not the box.
- **Oct 31, 07:00 · back to the old layout.** "you can probably use the old layout only for this hero section and
  then the form will stick when we scroll and freeze."
  → Keep the proven hero. Add new behaviour (the frozen form) below it instead of rebuilding it.
- **Oct 31, 08:10 · form first.** "i want to be abl to see the form ASAP." and "i want the header and the pink
  subheader bigger." The form moved into the hero under the headline; H1 went to about 66 px, the pink line to about
  40 px.
  → The whole form, button included, sits on the first screen of a 1440 x 900 laptop. Phones: headline, then form,
  then video.
- **Oct 31, 10:03 · the video column wide again.** "I want the column of the video to be bigger than the text
  column, just like before." → Video column about 1.44fr to 1fr. *Ana:* `grid-template-columns:minmax(0,1.44fr)
  minmax(0,1fr)`.
- **Oct 31, 10:03 to 11:45 · under the video.** Two columns of text were rejected: "I don't like this idea about
  two-column text. It just doesn't look great. I was thinking of putting the graphic here and not text." A three-day
  drawing went in, then the booking card came back ("can you put this back"), then "keeo this one too but less bulky,
  more compact".
  → Under the hero video: a graphic, never a second text column. Keep it slim and quiet.
- **Oct 31, 11:56 · sub line in sans.** "usesans srif here". → The line under the H1 is in the body sans; if the
  font has no real italic, emphasise with bold in the accent colour, never a fake italic.
- **Oct 31, 14:39 · headline much bigger.** "Wait, I meant the heading of the page: "How to Build the Income That
  Does Leave Your Job," not the "Save Your Seat" text." Claude had enlarged the form heading by mistake. H1 went from
  about 55 to about 80 px, four lines.
  → The H1 is the loudest thing on the first screen. When Sean says "heading", check which one in his screenshot.
- **Nov 1, 18:51 to Nov 2, 02:36 · the painted window.** "go ahead, use the shutter window." The video sits in a
  painted Greek window whose blue shutters open on load.
  - "I want the animation faster and smoother than this because they might just skip and scroll past it if it loads
    this slow, so we must really optimize the animation." → shutters open in about half a second on CSS from the
    first paint.
  - "I want it to be a little more 3D-looking because now it looks flat... I want more details on the flowers, on the
    flower pots, more graphic details." → painted edges, shading as they turn, shadows, a recessed video, geranium
    petals, seed heads, a Greek key band, ivy.
  → A hero graphic opens fast (about 0.5 s), reads 3D and detailed, and never touches the strip above it.
- **Nov 2, 05:15 · let it breathe.** "let's try to push down the slide with the CTA button and try to remove the day
  1, day 2, day 3 here. Because I think there's just too much going on. They won't be able to breathe." → The Day
  cards left the hero; the booking strip keeps a small even gap under the art at every width.
- **Nov 2, 06:06 · the video is the hero.** "I just need the video to be a little bigger." → Window about 5% wider,
  the flower box split out and shrunk, the logo on the video removed, about 20 px clear of the headline.
- **Nov 2, 05:43 to 05:46 · headline wording and breaks.** "revise the headline to: How to Build The (income or
  business?, which is better) That Pays You for What You Know in 2027". Claude chose "business" and said why. Then
  "looks a bit awkward. how to fix the line".
  → Break headlines on whole phrases only; set separate hand breaks for phones; the year never splits.
- **Nov 2, 06:14 · trust strip.** Made about 30% shorter, then sized to its content and centred over the video.
- **Nov 3, 07:31 · the Nov 3 headline.** Now a small pre-headline with the proof number highlighted, then the H1:
  "My Newsletter Business Has Made $1.4M. Here's What I'd Do First If I Wanted to Leave My Job in 2027." Then "i said
  you can make this bigger" (Claude had enlarged the wrong heading again) → about 69 px on desktop, about 55 px on a
  390 px phone, five whole-phrase lines on phones.
- **Nov 4, 03:25 to 03:34 · laptop fit.** The button fell below the first screen on short laptops. A centred version
  was rejected mid-build: "Is it even a good idea to put it in the center? Shouldn't it be the same, where everything
  is on the right? It looks really weird, like everything under the video. Shouldn't we keep it the same layout, but
  thinner, of course?" Moving the paragraph under the form was rejected too: "Even this one, the text underneath the
  form is still weird."
  → Tighten the approved layout first (thinner column, smaller gaps, compact form, H1 a little smaller only at 830 px
  tall or less). Supporting text stays above the form. The floating header button covers the rest.
- **Nov 4, 03:53 to 03:59 · the pill.** "The Exit Plan · Free 3-day event live on Zoom", with "live on Zoom" not bold,
  visible on laptops again.

→ Final hero spec: [registration-page.md](registration-page.md) section 5, [layout-type-spacing.md](layout-type-spacing.md)
sections 2, 4.1 and 11.

---

## 5. Forms, buttons and popups

### The sign-up form

- **Oct 31, 02:10 to 02:50 · narrow.** "I said, "Make the form thinner and narrower." It doesn't even have much
  stuff." 368, 292, 256 px wide.
- **Oct 31, 02:19 · plain is not enough.** "I think this form looks so basic. I don't like it there." It became a
  seat ticket: ink header, date tiles, chips, a perforated tear line, a "Seat holder" stub filling in the name.
- **Oct 31, 11:45 to 11:54 · then minimal.** "For the form, I still want to add first name and email. Can you make the
  form more minimalist? There's too much going on in it." and "also theres still too much stuff in there. you can use
  this" (his reference image).
  - Removed: the stub, "Admit one", date tiles, the dark header, the situation chips ("you can remove "where sre you
    right now" choices").
  - Kept: social proof on top inside the card ("Can you make the form narrower and put the testimonial bar on the
    top"), one date line, labelled fields, the button, the email note.
  - Shape came back without the clutter: "Can you use a better shape for the form, not just a mere rectangle?" →
    notches at a dashed tear line.
  → A form card is minimal in content but designed in shape. *Ana:* faces, five stars, "800+ student wins", tear line,
  two fields, button, note.
- **Oct 31, 11:49 · labels.** "add a label on form not just a blank with placeholder. first name. email."
  → Visible labels above every field, on every copy of the form, the popup included.
- **Oct 31, 12:39 · reads as a form.** "I want the form to look more like a form" → a clear heading, icons inside
  fields, firmer borders, a small lock by the email note.
- **Oct 31, 12:50 to 14:39 · the heading.** "Can you put back the save your seat here?" Then it got too big by mistake
  and went back to one line.
  → The form heading says what the form does and that it's free, on one line. A softer brand line can sit under it.
  *Ana:* "Save your free seat" over "Join me for all 3 days (for free)." (Nov 4: "Join me for all 3 days and add for
  free (inside parentheses).")
- **Oct 31, 13:55 · alive.** "Can you make this one sway sometimes or pulse, maybe?" and "Make the first black light
  up every now and then, like pulse the light around the black. Also, once they add their answer on first name, the
  email blank is also going to light up after."
  → The ticket swings a little every few seconds and stops for good once touched. A soft glow walks the eye from field
  to field to the button.
- **Nov 2, 02:36 to 04:04 · the hint got too strong, then too rare.** "I keep getting distracted by the light." It was
  softened and set to play twice; Sean then could not see it, so it now loops softly while the field is empty and not
  in use. *Ana:* `fhint 7s ease-in-out 2.5s infinite`.
- **Oct 31, 14:35 to 16:08 · size.** First the form filled its column ("I want the form to be scaled up like on the
  hero page. Maximize the width of the column."), then "I think the form is too big in height". → Full column width,
  compact height: fields 52 px (was 60), button 58 px (was 68), heading 36 px. Laptop form height 592 to 493 px.
- **Oct 31 to Nov 2 · one form, three homes.** One form moves between the hero ticket, a frozen rail on wide screens
  (1280 px and up, 284 px wide) and the popup. Bugs taught the rules:
  - an empty rail ticket showed beside the hero ticket → the rail fades in only when it holds the form;
  - "the form doesnt appear right away" → the rail takes over the moment the hero button slides under the header;
  - "why is this becoming blank when scrolling up?" → the form always goes to the ticket on screen; "don't move while
    typing" only holds while that ticket is visible. "make sure your fixes are not a bunch of patches and atually fix
    the right code".
  - "Maybe we can put this form in the middle, in the center vertically, so it would always be seen." → the rail is
    centred under the 74 px bar.
- **Nov 2, 02:36 · the ticket must never glitch.** "the form shape, the ticket shape around the form. It glitches,
  like it just disappears sometimes, especially when I click on it." → Draw the ticket as one SVG shape, not stacked
  drop-shadow filters over a mask.
- **Nov 2, 04:29 to 04:53 · "already in".** "Come on, you're really putting them into something. You're not just
  trying to get them in. It's like they're already in, they just have to sign up."
  → Forms feel active: a real "X just saved a seat" pill, a "Seat reserved for ___" tag that fills with the typed
  name, three ticks under the button (Free, 3 days live with me, Come as you are). Fewer words, not more.
  Names and counts come only from the real sign-up feed: names as soon as there is one sign-up in the last 3 days
  (the latest 8, first names only), the count once it reaches 50 (`FEED_MIN = 50`, was 100); until then the true
  fallback "800+ student wins".
- **Nov 2 · the popup.** Headline options were given after "give me variation here what even is this"; Sean picked
  "You're almost in. Just add your name." Then "make it a little less overwhelming because there's a lot of text
  going on", but "Also, for the form, don't remove the first name and email label."
  → Popups stay light. Labels are never removed. (Since Nov 3 the popup reads "Save your free seat." like the tickets.)
- **Nov 2, 06:06 · email checks.** "I also want you to add criteria in the email because sometimes they're just putting
  the wrong email." → Browser and server checks with one-tap fixes; let real people through when unsure. Full list:
  [ui-kit.md](ui-kit.md) section 8.
- **Nov 2, 06:36 · every button opens the popup.** "Can you show the pop-up form when they click any of the CTA
  buttons?"
- **Nov 2, 04:04 to 05:53 · exit popup.** Fires near the top edge (24 px) on desktop or on a fast flick up on phones,
  once per visit, never in the first 12 s or after typing. Fixed after "Is the "Don't leave yet" actually working?"
  *Ana:* "Don't go yet. Your seat's still here." / "Put your name on it before you go. It's free."

### Buttons

- **Oct 31 to Nov 3 · "free" on every registration button.** In the label or right under it, worded per section, often
  to the host by first name. *Ana:* "I'm in, Ana (it's free)", "I want my exit plan, free", "Show me where to start
  (it's free)", "See you live, Ana!" with "Free · Live on Zoom".
- **Nov 1, 18:57 · the less important half is smaller.** "(it's free)" is set smaller than the action words.
- **Oct 31 to Nov 1 · the sunflower.** "we can add a custom graphic on the left side of the button, like "I'm in,
  Anna." Something that, when you hover, is going to animate as well." On the VIP page: "Can you add the sunflower logo
  animation on the CTA button? It's just like on the registration page, in the form." → Every main button carries the
  brand mark on the left; on hover it spins and a dashed ring turns.
- **Oct 31 · shine stays inside the button.** A sweep that crossed the whole hero on phones was clipped to the button.
- **Nov 1 · a CTA in every section** (VIP first, then registration), worded for that section. Paid buttons show the
  price; free buttons say free.

→ Final specs: [ui-kit.md](ui-kit.md) sections 5 to 11.

---

## 6. Sections (registration page)

- **Oct 31 · sections follow the newest copy.** Each new copy doc reset the order; sections not in it were removed.
  Elements not in the copy were listed for Sean with the question whether they should stay. He removed the ticket extras and kept the stats and
  the student-wins bar.
- **Oct 31, 13:13 · the opening.** "Where is Anna's picture here? Also, this section looks very repetitive. There's
  too much text going on." → The questions as one big statement, her real photo beside "I'm Ana...", the button with
  its date, the edge-audience notes as a quiet row.
  → A section where the host speaks in first person shows her face. Fix repetition with a better layout, not trimming.
- **Oct 31, 13:13 · "Where are you right now?"** "Could you also improve this section here?... Better concept for that
  section." Plain options became illustrated choice cards that react to the pick and change the button words. Nov 1,
  19:50 they became painted scenes (a closed work laptop beside an after-hours notebook; a booked week with one slot
  turning hers; a signpost).
- **Oct 31 · results.** "Can you choose better testimonials with better results than these?" (52 subscribers was too
  weak.) Then Claude swapped the big numbers for weaker posts with screenshots: "Why are those small list testimonials
  different? Where's the 3,000+, 3,200, 2,400? Also, make the text maker show us that these are from the past
  challenge." Nov 3: "dont remove the other 2 testimonials here".
  → Lead with the strongest real numbers, labelled with their source and "Results vary". Never drop proof cards in a
  copy update without asking.
- **Nov 1, 10:33 to 19:47 · the Day 1 to 3 visuals.** "I want to put the real slides, real-ish, something built to
  intrigue people, secret sauce." First teaser images, then coded slides ("too generic"), then six painted slides, each
  with its own layout: "I still want the graphics to mean something, not just a bunch of things. I want them to be
  specific and have different layouts. I don't want them to look repetitive." Then "I love the slides, but the
  placements in it are not balanced." Then "I want Anna's face screen to have some variation, like have it different
  each day, like a different video frame maybe, and I want her face to show exactly."
  → Day windows play two real-looking slides as a live screen share, method covered, a different whole-face camera
  frame each day, in the window's corner.
- **Nov 2, 05:15 to 05:43 · day rows on desktop.** "You can probably widen some text on the top here since there's
  still a lot of space on the right." → Each row opens with date, headline and first line full width; the slide window
  stays in view beside the bullets.
- **Nov 3, 13:12 · the floating Day 1 to 3 bar.** "can you put this floating thing for days 1 to 3 under the
  top-right side instead, so it won't block the text while we're reading it? I think it's a little distracting. And
  annoying" → over the pictures, top right, about 20% smaller.
- **Nov 2 · the opening section beside the side form.** "I don't want to remove anything. I just need to be able to
  breathe because there's a lot of text." First pass shrank the type; "Isn't the text size a little bit too small?"
  → Add room, never cut content, keep type at reading size.
- **Nov 2, 03:23 to 03:45 · the fit check.** A road through the tick circles: "this execution looks weird". → One
  notebook page with ruled lines and ticks on the margin. Don't repeat a device from the section above.
- **Nov 2 · the "life left to enjoy it" calendar.** "you can add "money flowing around" or something here. Other than
  just the calculator, add the calendar." Then "Fix the calendar here. Update the dates. Why is it 5 days? It should be
  3." → Any mock app shows the event itself, real dates and number of days. (The section was later removed by the
  Nov 3 copy.)
- **Nov 3, 08:40 to 09:27 · "Why attend live".** "make these sans serif" (the questions), "make these text push
  through the right not just left aligned", "i thoght you were gonna fill up the right side", "still too much awkward
  white space in between", "make this sans serif. I'll review selected ideas live and show you what I'd change."
  → The split pattern: eyebrow, heading and first lines beside the picture (sized to that text), a dashed rule, the
  rest in two columns full width, then the button. Justified only on tablet and desktop.
- **Nov 2 to Nov 3 · the gift.** "I want some improvement to the concept of the graphic in your gift... Also, in the
  copy, can you say that this is like a calculator", then "cant see calculator", "The gradient behind it is a little too
  dark", "table can be more textured (and angled, not flat). it looks weird rn", "you can make bonus free gift img
  bigger and placed smarter".
  → Show the real tool readable (zoom to one card and the key number), say plainly what it is, lock the rest under
  "opens after you register", keep glows behind pictures, never behind text.
- **Nov 2 to Nov 3 · the prize.** "For the one-on-one with Anna, I was thinking of adding something into this, like
  Anna calling you one-on-one." "You can also improve the placement of this and make it 5 tickets." "make the tickets
  look better". "make 1:1 and session in the same line. also make it diff color or som. make it stand out like rly
  stand out" → "1:1 session" as a tilted hot pink label on its own line.
- **Nov 2 · reviews.** "can you animate and draw something like 5 stars on top, just small 5 stars, just so they know
  what the section is for?" Nov 3: review cards never split across columns (a stray shadow line showed).
- **Nov 3 · the final section.** The photo moved into an iPad frame (Nov 2: "This looks like a 2010 iPad"), then a
  new First Class photo shown at its own proportions, the calendar invite over the window row: "i said top right",
  "push a bit more to the right and a bit up. i wanna see the light", "you can push calendar (last section) a bit more
  down just above the lamp". Times per city with pins: "also say, so it would be clear: 12:00 pm if you're in New
  York · 9:00 am if you're in Los Angeles".
  Nov 4, 11:03 to 13:28: Ana asked to remove the AI First Class photo ("awful ... use one of the pics I gave you or a
  screenshot from my recording"). It became a still from her recording, then the real First Class photo Sean sent
  (`img/real/ana-cabin-real.webp`). Sean asked for an "iphone look"; a true-to-life iPhone with the Photos app open
  was rejected ("iphone ui doesnt look realistic", "dont use real iphone though i like the old size"), and the earlier
  tilted frame came back at its old size.
  → Client photos are her own, never an AI picture she has not approved; device frames stay simple, no app chrome.
- **Nov 4, 12:41 to 13:19 · the people she learned from.** First small face circles under "I've recorded
  conversations on my Substack with". Sean: "i kinda wanna show these instead like the actual video frames", "doesnt
  have to be on substack, just gotta tell ppl she got insights and had a convo from them too. make the design look more
  fit to the section and page", "use sans serif for their names", "and add a call graphic beside", "maybe not have to
  include kristina coz we don have vid of her". He offered "we can add logos of their stuff"; Claude declined (logos
  imply a partnership and clutter) and offered one credibility line each: "yes add short line of credibility too".
  Then "okok you can prob put this justin welsh pfp on his stuff coz its iconic", "for micheal why read tens of
  millions of times", "first. make sure all of em have the best bio here", "fix line". Final: "People I've sat down
  with, and learned from." under her story, six real call frames as small taped prints like her photo, names in bold
  sans with the green call icon, one checked line each, not clickable.
  → Proof from collaborations is real frames and the strongest line from each person's own pages; never logos, links
  or play buttons; no number whose sources disagree (Mary: 725 vs 722 weddings, so no count).
- **Nov 4, 12:41 · Marni's story.** Her own words from the live transcript open the reviews: "I went from 25 people on
  the wait list to 61 people on the wait list. Pretty much in two days." and "I already paid for my investment.", with
  a real frame of the live and "From Marni's experience in my bootcamp, said live with me. Individual results vary."
  The post title's "5x her investment in 7 days" was not used because the transcript does not say it.
  → A featured quote says only what the recording says.

→ Every section in its final form: [registration-page.md](registration-page.md).

---

## 7. The VIP page: from copy update to the bar (Oct 31 to Nov 2)

- **Oct 31, 13:42 to 17:08 · first changes.** A spam notice (sender named). Ana's story above the video and a 1-2-3
  "How it works" card under it. Headline B skipped the sentence that repeated it.
  → No sentence repeats its headline; every A/B variant is checked on its own.
- **Nov 1, 06:53 · facts follow the registration page.** "go through the entire VIP page and tell me if there's still
  some info that we haven't added or updated yet from the final copy of the registration pages." Day titles, times,
  the draw, "group" not "channel", no audience assumed.
  → When one page's copy is final, audit every other page against it, line by line, then give an honest opinion.
- **Nov 1, 13:48 · the Nov 1 copy, word for word.** "heres the new copy". The decline popups stayed as they were
  (his copy doc: "PROTECTED DECLINE FLOW" and "PRESERVE THE EXISTING IMPLEMENTATION").
- **Nov 1, 14:20 · the Fladlien redesign.** Sean's brief: "The goal of the page is to get them to sign VIP. That is
  the main, main, main goal... like they would sell it to themselves. You're not going to sell them, and you're not
  going to scold them". And "That's a designer's job, that's your job." Each VIP part shown working, a table built row
  by row, no button shimmer, the price modest and the package big.
  - Approval: "that's a really great way of applying Jason Fladlien's strategies visually. Props to that" and "I liked
    the areas where you put the design, like the decisions are right. Now we have to elevate the design".
  → Keep the placement decisions; later rounds lift the look. See [fladlien-on-pages.md](fladlien-on-pages.md).
- **Nov 1, 14:33 to 15:06 · not "made by Claude".** "right now it looks like a generic Claude design... I don't want
  people to be able to catch that this was made from Claude... I want it to feel like Ana, like a human designer
  designed for Ana". Claude was stopped twice to study the references properly: "don't just review the texture, but
  review the form: the shapes in it, the lines, the creativity captured."
  → Study every reference for form, value and where colour lives before drawing. Colour only on the story. Every
  picture painted in code; Pinterest images off the site.
- **Nov 1, 15:10 · real vs painted.** "in some areas that require more specificity and raw stuff other than metaphor,
  we can start to create the raw stuff (like the raw screenshot, if needed, or the raw material). You tell me which
  stuff has to be raw" → Real screens on painted devices for anything that proves what they get; paintings for
  feelings.
- **Nov 1, 15:08 to 16:03 · the background.** Warm cotton paper over the page, then calmer, then "I still don't really
  like how the background looks. It looks a little cheeky", then flat and calm, then "use the textures and the mixins I
  gave to you earlier, but not in a way that it's too solid. Maybe just use those as reference and put your own
  textures subtly in sections".
  → A calm white base; subtle code-made textures per section; brand colour in shapes, not whole fills.
- **Nov 1, 15:32 · balance and repetition.** "Some of them are too scattered. Some of them are too tight. Make it more
  balanced. Sometimes the text doesn't fit in where they are." and "The UI right now is a little bit generic-ish and
  repetitive." → One focal device, two props, clear margins; vary how sections open; remove repeated decoration (the
  stamp strip over every item became one index rail).
- **Nov 1, 15:32 to 16:03 · motion.** "Probably instead of creating the graphic as it is, I should already plan an
  animation for it instead of just creating static visuals." → Motion rebuilt with GSAP (self-hosted): the props act
  out each line, play once in view, small idle loops after.
- **Nov 1, 16:08 to 17:38 · the details round.**
  - "can you remove the example annotation" → no EXAMPLE stamps on recreated screens.
  - "Can you also remove the "group members can see each other's phone numbers" example annotation?", later its
    replacement line too.
  - The Sprint: "I want to use your actual screenshot, not this rebuilt one, and I want to use the mockup that I sent
    you, the full-on mockup." → the real screen, big, zooming in.
  - The chair in the fit check, three rounds: "I want this seat, this chair, to move faster because there's too much
    delay right now." A CSS transition was fighting the GSAP tween, then it moved while its card was still fading in.
    → Start an object's move only once its card is well in view, with a travel you can see.
  - "Where is the Q&A? ... That should be part of the features." → the Friday session named "VIP Q&A and review"
    everywhere, with a "Live VIP Q&A" tag.
  - The Q&A window: "The UI for the VIP queue kind of looks gay", "It could look more realistic." → a faithful Zoom
    Question and Answer window in Zoom's own blue. Approved: "Okay, publish. You did amazing, sweetie."
  - WhatsApp: "Use the exact WhatsApp I put in her breath colors and breath in general." ("breath" is voice typing for "brand") → the exact layout, themed in
    her colours, with the real VIP group picture. Approved: "Beautiful, beautiful."
  - "the stuff you put in bold is not really even that important. You can make the sentence bold, and the other
    sentence that relates to this is similar in terms of information. not just highlight, bold too"
  - "I want the graphic to visually convey that a little bit more literally. Maybe you can add it somewhere in the text
    as an animation" → "access expires: never", written in by hand.
  - "I want to make the spam and promotion reminder at the top be scaled down a bit more." and "I want an arrow
    animation on there to make them scroll to the VIP page so it becomes the focus."
- **Nov 1, 17:38 · the verdict.** "this is fucking the most perfect VIP page we have ever built, you have ever built
  in history". The VIP page is the reference for every page that follows.
- **Nov 2, 07:37 · the lifetime seal.** It hung off the buy box: "looks wrong". → Inside the box, beside the price.

→ Final VIP spec: [vip-page.md](vip-page.md).

---

## 8. The registration page after the VIP page (Nov 1, evening)

- **The mistake.** Claude rebuilt the registration page in the VIP page's finish. "You honestly kind of ruined it. I
  prefer the old colors, deign, and you stripped away a lot of stuff, basically. I'm not a fan. Can you bring back the
  charm?"
- **The fix.** The original was restored at once (cream, ink-outlined drawings, iPhone video, Day windows, pink
  buttons) and the VIP techniques were layered on: key lines bold and highlighted, a CTA per section, the sunflower on
  every button, the Day 1 to 3 tracker, the slide wall, the painted scenes. Sean's scope: "I just want you to implement
  what you did on the VIP, add on top, and maybe replace some graphics that could look better with our new
  techniques."
- **Then the effort bar.** "the graphics you're making right now are too generic, and you didn't put as much effort in
  as you did in the VIP graphics. they are also not specific and not animated premiumly" and, on pace, "Are those
  literally all that you've done after 20 minutes?" and "go ahead with all six, send each one as done. one should only
  take 8 mins max."
  → An approved page is upgraded additively. Every new graphic gets the effort of the best page in the funnel.

---

## 9. Graphics, colour, photos and badges

- **Grounds.** Oct 25 a light warm grey. Nov 2: "im not a fan of this puke poop grey color they dont really go well".
  The sand fill and texture overlays went; sections now use her cream, a sunflower cream or blush.
  → Section grounds come from the client's fresh palette tints, never muddy beige or grey.
- **One background idea per section.** "Not just colored shapes, but actually think of a unique background for that
  specific section." *Ana:* skies that move from sunrise to sunset across the three days, a pinboard for the wins, the
  call rings around the 1:1 phone. The village skyline left the hero for the footer: "these can be moved maybe on the
  footer instead so it wont look overwhelming."
- **Proof that looks real.** "I want that to look a little bit more like a raw screenshot instead of something like
  this. It looks Claude-generated if we keep it like that." → a compact Google Ads-style overview; no hand-drawn
  loops on UI replicas. "make these look more like raw testimonials. Are there screenshots for this?" → real
  screenshots or the note word for word; never drawn mockups as proof.
- **Money you can see.** "Maybe make them more excited about it." → $100 notes counted out in rows while the amount
  counts up, instead of dots.
- **Annotation arrows.** "I also want you to fix the arrow because it looks like every other Claude annotation ever.
  Fix the arrow and make it look cuter." → a dotted hand doodle with one loop to a taped tag.
- **Real app icons.** "By the way, this is the Google Calendar logo … customize it with our date at 8 and customize
  the colors, but use this exact shape. and form". For FaceTime Claude declined a copy: "i need it green though thats
  he color that associates" → an original green gradient circle with a solid white camera.
  → Use a familiar app's shape and colour association, never a copy of a trademarked icon.
- **The host's art as a sticker (Nov 3).** "noo i was thinking an svg custom claude made version of that, also
  transparent background ... like a sticker", "dont be lazy, add more effort on the curves. you can put line on top of
  it first", "dont remove the curves and textures of the leaves and flowers", "can you make the outline more raw hand
  cut", "can you cut this big white area". → Trace over the reference, check zoomed, keep every curve and texture, cut
  a raw scissor edge. Still to do: the remaining leaves.
- **The signature (Nov 3).** "I want the signature to look more like a signature, but still, her name should be
  readable." Fonts tried, then Meddon traced; "make the signature animation faster" (about 1 s); ink colour from navy,
  to red, to dusty rose, to "use the pink of the page instead"; the wordmark under it "looksbad, put it on side
  instad"; "signature should be pushed up a bit so its balanced".
  → A real, readable signature in the page's own accent, writing itself in about a second, the wordmark beside it.
- **The painted frame (Nov 3).** "should we make this a picture frame in our graphic techniques instead. not a
  rectangle yelllow and white" and "make sure this aint cut". → Painted frames, never flat rectangles; give paintings
  room so shadows are whole.
- **Photos of the host.** Real photos only; Gemini edits keep her face and get a finishing pass ("What the hell did
  you use for the photo finish pass? How did it look more like her? Yes, use this."). Device frames are current
  models, kept simple. Nov 4: Ana rejected the AI First Class photo ("awful ... use one of the pics I gave you or a
  screenshot from my recording") and Sean rejected app chrome around it ("iphone ui doesnt look realistic"). See
  section 6.
  → Never ship an AI picture of the client she has not approved; no app chrome around a client photo.
- **Badges (Nov 2).** Sean's idea: "Once you slap this in somewhere, suddenly your monkey brain gets activated ...
  Obviously, you should not overdo this". Gemini makes them from a better prompt ("No, I still want Gemini to do it,
  but something that looks a little better. I want you to make the prompt better."); "looks bad. looks gemini
  pattern haha" led to glossy traditional seals; "i dont wanna add full frefund" kept the promise badge honest.
  → At most about two per page, on the corner of what they label, never over copy.
- **Christmas (Nov 2).** "Just a little cute seasonal spice try to think of where we can add this Christmas stuff."
  → Small touches on brand pieces, one date-gated script, painted with the house technique ("christmas tree and other i
  prefer using our graphic techniques"), snow only in two sections ("I don't need the snow to fall across the whole
  page because that might be too distracting").
- **Christmas, lighter (Nov 4, 11:03 to 13:15).** Ana: the page "looks very christmasy". Sean: "less christmas stuff".
  The first cut took off every Santa hat, the lights on the form and the hero snow. Sean brought two back: "keep the
  xmas sunflower on the buttons lol" and "and the lights on form". Final: the hat on every button's sunflower, the
  lights on the frozen form, the wreath, the footer village lights, holly on Day 1, snow in the last section; no hat
  on Ana in the header, no hero snow. Greek people do celebrate Christmas, so the layer stayed.
  → Dial a seasonal layer down by cutting places (the host, the big moving pieces), keep the small touches on brand
  pieces, and check the holiday is the client's own.

→ Rules: [../graphics.md](../graphics.md), [ui-kit.md](ui-kit.md) section 13.

---

## 10. Motion

- **No pops, slides or pulses.** "I don't want pops, pulses, and slides. I don't want any of that. I want it to be
  smooth" and, on the VIP page, "Where are the animations? I think these are just slides and flaps. Where are the real
  animations?"
- **Planned with the picture.** Each picture acts out its line once when it comes into view; nothing moves while its
  card is still fading in; the animation library owns any transform it animates.
- **Fast at the top.** Shutters about 0.5 s; the "Bring the part you're stuck on" scene went from about 8.6 s to about
  4.5 s ("And make the animation faster on the part you're stuck on."); the signature about 1 s.
- **Cheap to run (Nov 4).** Pulses, glows and shine rebuilt with transform and opacity only; snowflakes drawn once to
  a bitmap.

→ [motion-and-speed.md](motion-and-speed.md), [../motion.md](../motion.md).

---

## 11. Copy

- **Word for word, every time.** Sean's docs arrived Oct 31 (three versions), Nov 1 and Nov 3. Each was put in word
  for word, then checked line by line. Only dashes change: "here's the updated registration copy (dont use em
  dashes)". Date ranges written with an en dash became "Nov 17 to 19".
- **Skimmable.** "make it skimmable, add some bold and highlights, and know which words to emphasize (which words are
  important for them to get to opt in)". Then "make the highlight a bit subtler". → Bold plus a soft yellow band on the
  lower part of the key line only. *Ana:* `rgba(255,212,0,.42)` at 34% height on the fit check.
- **First person.** "can you make it a little bit more first person? ... I want Anna to be the one talking here." →
  "From people in my past challenge", "worked with me".
- **Numerals.** "can you make it three (3) just for them to visualize the number 3, not just as a word also, anywhere
  where we say a number, not everything, but you can do this in the most appropriate cases."
- **No promises, no replays, no program pitch** on the free pages; prize copy carries no value the copy doesn't give
  (the old "worth $3,000" went).
- **Deviations are reported.** After the Nov 3 pass two result cards were missing and Sean had to ask. → List every
  dropped section, invented micro-copy and dash change after a copy pass.

→ [copy.md](copy.md).

---

## 12. Time zones and dates

- **Nov 2 · dates moved.** "can you change the dates to December 8th as day one? tuesday." Every date moved +21 days
  across every page, file and image; the program's Round 1 dates were asked, not guessed. Nov 4, 13:34 caught the dates
  still baked into images.
  → A date move is funnel-wide, images included; then check every live page for old dates.
- **Nov 4, 01:40 to 03:09 · the visitor's own time, in five steps.**
  1. New York plus "your time". Claude shortened times to fit: "dont remove the 12:00 zeros. that kind of sets them
     more up than 12pm only."
  2. Claude suggested the visitor's time only; Sean: "coz well have to say new york in emails and stuff." → both, New
     York as the anchor.
  3. "How about instead of "your time," say "Manila" instead, because they might think it's not real?" → the city name
     from the device time zone.
  4. "Don't remove the free workshop, a free 3-day live event, from the header (sticky header)."
  5. "I think there's just too much bolded text on the sticky header right now, so I think we should prioritize their
     time instead, or at least make that bigger and put it on top... Maybe the colors are too sharp." → the visitor's
     line bold on top with a soft highlight, New York small and grey under it, a tiny pin before the city ("You can
     probably put a TINY location graphic for your specific location.").
- **Nov 4 · forms.** "Also, highlight it on the forms or make it bigger or something, because time is a little bit
  important here." → "For you: Wed, Dec 9 · 1:00 am in Manila" with a small clock. "Why not in the same row as the
  pink "Free 3 Days Live"?" and "How about if you put the December 8-10 New York under the December 9 instead of under
  the free 3 days live?" → their dates in the pink row, New York tight under them. "fix spacing looks a bit bad" →
  phrases never split.
- **Nov 4 · day cards** show the visitor's weekday, date, time and city first, New York beside it in grey.
- **Nov 4, 12:19 to 13:22 · the session times.** Their city big and highlighted on top, their dates with New York's
  beside (under on phones). Pros and cons of keeping the other cities were discussed; Sean: "how about add an area
  for those but make their city the highlighted bigger one", then "make it 2 per column instead". → The other cities
  stay, small and grey, on an "Also:" line, two per row; all four as before when the zone is unknown.
- **Nov 4, 13:21 · every other date and time.** Sean: "fix these dates as well make them adaptable", then "and these.
  any more mention?" → the date tiles, the booking strip ("1:00 am in Manila / 12:00 pm New York"), the line under
  the hero button, the closing ask, the calendar invite (as their own calendar would show it), the thank-you line, the
  phone bar and the header's short date all follow the visitor; New York and unreadable zones see the original. Their
  dates on the forms got bigger ("make date bigger here", `1.32em`).
  → Search the whole page for every date and time and make each adapt, not only the ones Sean points at.
- **Still to do:** the cities in the final list come from audience data ("from her survey if there is som where they
  come from. the majority."); the phone bottom bar shows their dates but needs their time and city ("Shouldn't the
  phones also have the date line? Isn't that important?"); the popup has no "For you" line and its eyebrow turns all
  pink in time-zone mode (judges, Nov 4).

→ [ui-kit.md](ui-kit.md) section 15.

---

## 13. Speed (Nov 4)

"I want them to load as fast as possible, really fast, without removing anything from them. Same quality, same high
quality. Maybe there's a different way to make it faster."
- Images resized to the sharpest size they show at (many were 3 to 13x too big), AVIF for painted art with WebP
  fallback, small decorations lazy-loaded: 2.7 MB to 1.8 MB of images.
- Fonts self-hosted; cache headers; work folders kept off the public site.
- Measured live: hero first painted at 2.0 s, now about 1.1 s, full load 3.2 s to about 1.9 s, layout shift 0.06 to 0.
- Big monitors (from 1800 px wide) scale the page evenly: "Yeah, I think we can scale for big monitors, for sure."
  Laptops never scale up.
→ Still in progress. [motion-and-speed.md](motion-and-speed.md) section 11.

---

## 14. Reversals that teach something

| what was tried | what Sean said | what won | the lesson |
|---|---|---|---|
| Editorial full-width hero, headline about 100 px | "making the heading a little smaller? It's too big" | The old two-column hero | Keep the proven layout; add behaviour beside it |
| Seat ticket with stub, tiles, chips | "Can you make the form more minimalist? There's too much going on in it." | Minimal ticket, notched shape | Design the shape, not the clutter |
| Rebuild of the registration page in the VIP finish | "You honestly kind of ruined it." | Original restored, VIP techniques on top | Improve on top, never strip |
| Pink strip scrolling away | "No, I don't want the pink strip to scroll away." | Strip inside the sticky header | A warning that matters stays visible |
| Coded Sprint player | "I want to use your actual screenshot, not this rebuilt one" | The real screen and his mockup | Real proof beats a rebuild |
| Results swapped for posts with screenshots | "Where's the 3,000+, 3,200, 2,400?" | The strongest real numbers, labelled | Never trade strong proof for weaker proof |
| Visitor's time only | "coz well have to say new york in emails and stuff." | Visitor's time on top, New York under it | Pages must agree with the emails |
| Centred hero for laptops | "Shouldn't we keep it the same layout, but thinner, of course?" | Same layout, tightened | Tighten before rearranging |
| Paragraph moved under the form | "Even this one, the text underneath the form is still weird." | Paragraph above the form | Fold position is not worth a broken reading order |
| Pulse played twice, then stopped | Sean could not see it | Soft loop every 7 s while empty | Subtle beats strong, but it must keep showing |
| A true-to-life iPhone with the Photos app around her photo | "iphone ui doesnt look realistic", "dont use real iphone though i like the old size" | The earlier simple tilted frame, old size | No app chrome around a client photo |
| Every Christmas hat and the form lights removed | "keep the xmas sunflower on the buttons lol", "and the lights on form" | Hat on the buttons and lights on the form back; no hat on Ana, no hero snow | Cut the big pieces, keep the small brand touches |
| Face circles under "I've recorded conversations on my Substack with" | "i kinda wanna show these instead like the actual video frames" | Real call frames as prints, no platform named | Real frames beat names and faces |

---

## 15. Still to do (as of Nov 4)

- Phones and tablets pass (portrait and landscape): graphics, layout, the bottom bar with the visitor's time and city
  (their dates are in since Nov 4); whether the bottom bar keeps "(it's free)" below 390 px.
- Found by the judges on Nov 4: the popup email typo check lets a mistyped address through on the same click; the
  phone bottom bar overflows at 390 and 320 px and lacks the visitor's time; the popup has no "For you" time line and
  its eyebrow turns all pink in time-zone mode; the side form breaks "About 90 minutes a session"; the day map covers
  text in the Day 2 row; on a 320 px phone "Save your free seat" runs past the edge.
- Cities for the session-times list from Ana's audience location data.
- The video: page window is about 1.548:1, so decide window vs render ratio before the final render; a silent loop
  and captions; Ana's own voice.
- The painting sticker: middle cluster, lower leaves, tendril.
- Ana's real screenshots to replace redrawn proof (the 771 and 82 like posts, the two-sale workshop page).
- Link preview images in square and 16:9; noindex off on launch day.
- VIP: the "one morning slot" wording, a testimonial near the price, and Sean's open question whether the page
  over-applies Fladlien.
- Speed work continues.

---

## 16. Lessons that generalise

1. **The first approved layout is usually right.** When something doesn't fit, tighten it (narrower, smaller gaps,
   smaller only on short screens). Rebuilding the hero cost a whole night on Oct 31 and ended where it started.
2. **Improve on top; never strip the charm.** A page Sean approved keeps its colours, drawing style and sections. New
   techniques are layered in. Keep removed graphics in git; he often asks for them back.
3. **Every page serves one goal.** Registration: the opt-in ("the purpose of this page is to get them to opt in.
   That's it."). VIP: they choose VIP themselves, without being sold to or scolded. Judge every element by it.
4. **Show, don't describe; real where it proves, painted where it's a feeling.** Real screens, real numbers, real
   photos; painted metaphors for what hasn't happened yet. Apps people know are copied faithfully and themed, never
   their trademarked icons.
5. **It must not look made by Claude.** Study the client's world and the references for form, not only texture.
   Colour on the story, not the page. Thick borders, hard offset shadows, flat icons and generic arrows read as Claude.
6. **Minimal content, designed shape.** Forms, tickets, cards: few words, every one doing a job, in a shape that
   belongs to the brand.
7. **The form is always in reach.** On the first screen, frozen beside the page, in every button's popup, and on the
   exit. One form, never two, and it never shows empty.
8. **Remind them it's free, everywhere, in their voice.** And name the host by first name on the buttons.
9. **Time is for one person.** Their date, time and city first, the anchor zone under it, full ":00" times, phrases
   that never split.
10. **Motion is fast, planned and cheap.** Above the fold in about half a second; each picture acts out its line once;
    only transform and opacity; nothing nags.
11. **Copy is the client's, word for word.** Make it skimmable with bold and soft highlights; report every deviation;
    no em dashes; numerals after key counts; first person for the host.
12. **Check what Sean means before changing it.** Twice the wrong heading was enlarged. Read the screenshot, name the
    element, and say which reading you took.
13. **Fix root causes and test every path.** The blank hero ticket and the vanishing ticket shape were both fixed in
    the code that decides the behaviour, not with overrides.
14. **Proof about people is real and checked.** Real call frames, never logos or links; the strongest line from each
    person's own pages; a quote says only what the recording says; a client photo is her own.
15. **Branch first, publish on the word, check live.** Nothing goes live until "publish"; after it, check every page
    on the live domain at desktop and phone. See [page-sop.md](page-sop.md).

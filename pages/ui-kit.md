# Page UI: header, forms, buttons, popup, bottom bar, tickets, badges, small pieces

Every small UI piece on a funnel page, and the rule for each, so a new client's pages come out right the first time in
their own brand. Each rule is general; Ana Calin's Exit Plan pages (registration `2026-ana-calin/index.html`, VIP
`2026-ana-calin/vip/index.html`, offer pages `program/` and `join/`) are the worked example, with exact copy and
selectors. Where Ana's value is a placeholder for a brand choice, swap in the client's own (colour, mark, fonts, voice).

Related: `registration-page.md` (section order and jobs), `vip-page.md` (the VIP header, buy box, decline flow),
`layout-type-spacing.md`, `copy.md`, `motion-and-speed.md`, `fladlien-on-pages.md`, `page-sop.md`, `evolution-ana.md`.
Playbook rules this builds on: `../graphics.md` sections 5 to 7 (badges, UI pieces, seasonal), `../motion.md`,
`../SOP.md` (checks and publishing), `../clients/ana-calin.md` (her facts, colours, marks).

## 1. Shared basics for every piece

- **One accent runs the UI.** The client's signature colour is the main accent on all their pages: buttons, highlighter
  marks, badges, the countdown's seconds, rings and dots. Light accents (yellow) take dark ink text. Small accent text
  on a light ground uses a darker shade of the accent so it reads.
  - Ana: sunflower `#FFD400` with ink `#1A1412` text on buttons; hot pink `#F72585` as the second colour (taglines,
    pins, dots, field glow). The header's small caps use a darker pink `#D81B6E`. Sean: "Can you make yellow more of
    the main color instead of pink?"
- **The client's mark lives on the buttons** (section 11) and in the header (the favicon character). Use the client's
  own motif, never a generic icon.
- **The soft highlight** (a marker band behind the lower half of the words) is the one way to make a line stand out.
  Use the page's own highlight; never invent a sharper colour for one piece. Ana: `rgba(255,212,0,.38)` to `.6`,
  from about 45 to 55% down to 90 to 92% of the line height.
- **Sans for numbers, dates and small labels;** the display serif only for headlines and soft taglines
  (`../README.md` rule 6). If the serif has no bold, set bold bits in the bold sans instead of faking bold.
- **Nothing covers text.** No sticker, badge, tag, pill, camera tile or logo sits over a headline letter, a number or a
  line of copy, at any width. When a small asset crowds or blocks something, move it to the side, into genuinely
  empty space or onto the corner of the thing it labels. Check desktop and 390 / 320 phones.
- **Real data only.** Counts, "just joined" names and tickers show only real numbers from the email platform
  (`../SOP.md` E). No invented registrant counts.

## 2. The floating header (registration and offer pages)

**What it always shows** (left to right): the client's cartoon or favicon, the event name with its offer line
("A free 3-day live event"), the bold date and time line, a countdown, and one button that says it is free. On a paid
offer page: the program name, the deadline and one accent button.

- **Shape and material.** A floating rounded card, not a full-width bar: sticky at the top with a small gap, about
  half the room of a full bar. Light frosted glass with depth, never a flat dark pill: a translucent pane that blurs
  what is behind, faint brand tints in two corners, a bright white top edge, a soft shine on the upper half, a
  two-layer shadow with a hint of brand colour, dark ink text. Sean on the dark version: "There's no depth." and
  "I'm not a fan of the color". Verify the blur in a real browser: test screenshots often do not show it.
  - Ana: `header.fb > .fb-bar`, sticky `top:0` with `padding:12px 16px 0`, `width:min(1080px,100%)`, radius 16px,
    pink tint top left `rgba(255,184,217,.35)`, yellow bottom right `rgba(255,212,0,.22)`, `blur(20px)
    saturate(1.8)`, shadow tinted `rgba(150,40,90,.25)`.
- **Icon.** The page favicon (the client's cartoon), cropped tight on the face and brand mark, no white edge. When an
  image changes, save it under a new file name so browsers do not show the cached one (the mascot rules: section 17).
  Ana: `img/o/fav/header-ana.webp`, 44px, radius 12px (40px round when slim). Sean: "I also want you to use the favicon of the page, the cartoon Anna,
  on the sticky header on top." then "Also, I said to zoom this in, right?"
- **Event line.** Sentence case (all caps wrapped and cut), one line, in both the full and slim states. Never remove
  the event name or its free offer line, even to fit time information: make the bar taller or move other text. Sean:
  "don't remove the free 3-day workshop on the sticky header" and "Don't remove the free workshop, a free 3-day live
  event, from the header". When space runs short the page measures it and drops whole phrases, host name first; never
  cut mid-word. Check 901 to 1600px in both states.
  - Ana: `.fb-t small`: "The Exit Plan" + `.fb-w` " · A free 3-day live event" + `.fb-w2` " with Ana Calin" +
    `.fb-dt2` " · Dec 8 to 10" (shown when there is room). 11.5px, weight 800, `letter-spacing:.18em`, pink
    `#D81B6E`. The fit script drops `.fb-w2` first.
  - Still to do: the fit script can also drop `.fb-w` (the offer line) as a last resort at the narrowest bar, which
    conflicts with Sean's rule. Check whether it ever fires between 901 and 1600px and stop it if it does.
- **Date line.** Bold, in the bold sans: dates and time with the anchor city. Ana: `.fb-t b` Manrope 800, 17px:
  "Dec 8 to 10 · 12:00 pm New York". Sean: "Also, make the dates bold." For visitors outside the anchor zone see
  section 4.
- **Button.** The same free button as the form (section 11), smaller. Keep "free" on it even when space is tight:
  tighten chips and spacing instead. Sean: "Don't remove for free." Ana: `.btn.sm` "I'm in, Ana (it's free)".
- **Every part of the header opens the sign-up.** The icon and title are one button (`.fb-id.open`) as well as the CTA.
- **Shrink on scroll.** After about 160px of scroll it slims into a narrower pill (CSS transition, about 0.45s) and
  grows back near the top (Ana: in at `scrollY > 160`, out at `< 90`, class `.fb.min`). Slim is still readable, not
  tiny, and keeps every key element: icon, event line, bold date line, countdown, the button with "free".
  - Ana slim: `width:min(704px,100%)`, radius 999px, about 52px tall (button 42px + 5px padding), icon 40px, date
    14px, countdown digits 14px with one-letter units (d h m s). Sean went narrower several times ("can I make the
    sticky bar a lot more narrow, thinner, and smaller once I scroll, more compact?"), then back up when it got too
    tight ("countdown is a little bit too tight"). Tell Sean when you reach the narrowest possible without dropping
    an element.
- **Height.** Same height as the original unless content needs it. It may grow for a second time line only when the
  visitor's place is known and differs from the anchor zone (section 4). Sean: "only when they have location
  avaialble. if only new york then keep the sticky header height".
- **Phones.** No floating header at 900px and below (Ana `@media (max-width:900px){.fb{display:none}}`); the phone
  bottom bar (section 10) replaces it, so the two never stack. On an offer page the pill slides away once the bottom buy bar appears.
- **Not in the header:** a join count or extra badges crammed in. One button only.
- **VIP page header:** a different job (keep them on the page, show the step). See `vip-page.md` section 4: glass
  pill, "Don't close this page" pink strip inside the sticky card, the VIP favicon, three steps with "Step 2 of 3",
  never the word "optional" on the upsell step. Sean: "On the sticky header, you don't have to put "optional."
- **Offer page header:** the same floating pill with the program name, deadline and one accent button (Ana `/program/`
  and `/join/`: `.pbar`, "The Exit Lab", button "Start my offer"). Sean: "Can you try to make the header a sticky
  floating header as well, because I think it's taking up too much space this way?"

## 3. The countdown

- A live countdown to the first session, computed in the event's anchor time zone. Ana: to Tue Dec 8, 12:00 pm New York
  (`Date.UTC(2026,11,8,17,0)`), `.fb-cd`.
- **Label on top, inside the same chip:** a short "coming up" label, better than "days left", with a round pulsing
  accent dot that is never clipped into a pill or "D" shape, in full and slim states. Ana: "Starting soon" (`.fb-cdk`)
  with a pink dot. Sean: "For this sticky header timer, I want you to put "days left" on top, or something better than
  that." In the slim bar the label folds away and the units shrink to letters.
- **Numbers:** bold, clear sans (never the display serif), tabular figures. Unit labels sit tight right under the
  numbers, no gap. Parts have clear space between them. Seconds on the accent. Sean: "i want the numbers to be clearer
  and sans serif", "Can you put the label underneath? Stick more to the numbers, so there's no weird gap in between."
  - Ana: `.cdu` white glass chips 46 x 46px, digits Manrope 800 19px, labels 8.5px caps ("days", "hrs", "min",
    "sec"); the seconds chip `.cdu.s` is solid sunflower.
- **Narrow screens:** the whole header hides at 900px and below, countdown included. The phone bar carries the date
  and "Free and live on Zoom" instead (section 10).

## 4. The visitor's time in the header

- Visitors outside the anchor zone see **their** dates, time and city as the one bold line, with the soft highlight; the
  anchor time sits directly under it, smaller, lighter weight, warm grey. Only one line in the header is bold. Visitors
  in the anchor zone, or with an unknown zone, see the original header at its original height. Sean: "I think there's
  just too much bolded text on the sticky header right now, so I think we should prioritize their time instead" and
  "Maybe the colors are too sharp."
  - Ana (`.fb-t b.fb-two`): "Dec 9 to 11 · 1:00 am in [pin] Manila" bold with highlight `rgba(255,212,0,.38)` from 55%
    to 90%; under it `.fb-ny` "Dec 8 to 10 · 12:00 pm New York" at `.74em`, weight 600, `var(--ink3)`, margin-top 1px.
- A **tiny** map pin before the city, the same pin used elsewhere on the page, sized to the text (Ana `.fb-pin`,
  `.78em`, pink). Sean: "You can probably put a TINY location graphic for your specific location."
- On narrow bars the visitor's phrase drops whole onto its own line (`.nw` spans); the bar never cuts a word.
- How the place is found, and the wording rules, are in section 15.

## 5. The sign-up form: one form, three homes

- **One form, not copies.** The same `<form>` moves between the hero ticket, the frozen side ticket and the popup, so
  typed text, checks and the personal seat line move with it. Ana: `#join` moves between `#hslot`, `#rslot` and the
  popup `.dlg` (`homeSlot()` / `placeForm()`).
- **Seen at once.** The form sits in the hero on the first screen, right under the headline: on a 1440 x 900 laptop
  and on phones (on phones it sits in the page under the headline, before the video, not only behind a popup; still
  to do: re-check this in Ana's phone pass, since the hero was rebuilt after the rule was set).
  Re-check the fold after every copy or form change. Sean: "i want to be abl to see the form ASAP."
  - Ana: at 1440 x 900 the ticket fills the column (531px) and its button sits just under the fold; the pinned header
    button covers that. On a short 1280 x 720 screen there is about 100px of scroll where the hero button is
    just below the edge before the side ticket takes over; left as is.
- **Frozen side ticket on wide screens.** From 1280px wide, the form follows the scroll in a slim column on the right,
  from below the hero to the final section, so it can always be seen. Sean: "I want to freeze the form on the right
  side ... Since Anna's form is simpler, we can make it thinner, slimmer, so there's more surface area for the page
  content itself."
  - Width: narrow, because the form holds little, but big enough for comfortable fields. Ana: `--rw:284px`.
  - Vertical position: centred in the space under the floating header (equal gap above and below), with a minimum
    clear of the header. Ana: `.tksticky{position:sticky;top:max(92px,calc((100vh + 74px - var(--tkh,480px)) / 2))}`,
    `--tkh` measured from the card. Sean: "Maybe we can put this form in the middle, in the center vertically, so it
    would always be seen." Check at several laptop and desktop heights.
  - Hand-over: it takes over as soon as the hero form's button slides under the floating header, and fades in fast
    (about 0.2s; Ana `.v2rail.on`, `.18s`). It only shows once it holds the form, so an empty ticket never sits
    beside the hero ticket. At the very end it scrolls away and hands over to the final section's own button, with
    the header button still there: never a moment with no form or button on screen. Sean: "the form doesnt appear
    right away".
  - The form always goes to whichever ticket is on screen. The "do not move while typing" guard applies only while the
    ticket being typed in is still visible. The hero ticket never shows an empty space. Sean: "why is this becoming
    blank when scrolling up?" Test: plain scroll, typing in the side form, clicking a side field, opening and
    closing the popup, Escape.
  - Below 1280px: no side ticket; one column, and buttons open the popup.
- **Every CTA opens the popup.** Every sign-up button on the page (header, hero strip, each day, each section, final)
  opens the popup form, on desktop and phones, instead of scrolling to a ticket. The tickets still work if someone
  types straight into them. While the popup is open the ticket behind keeps its size (no jump); closing puts the form
  back. Sean: "Can you show the pop-up form when they click any of the CTA buttons?" Ana: every button with class
  `.open`.
- **Size.** The hero ticket fills its column with comfortable fields; the content stays minimal. Compact in height:
  fields about 52px, button about 58px. Sean: "I think the form is too big in height". Ana hero `.htk`: inputs 52px
  at 17px, button 58px at 18.5px; at 1440 the form shrank from 592 to 493px tall. Side ticket inputs 43px, button
  50px.
- **Phones:** the form fills the screen width; inputs stay at 16px or larger (stops the iPhone zoom on tap);
  placeholders must fit fully on the smallest phones.

## 6. The ticket shape

- A sign-up form is never a plain rectangle: it is an event ticket. Sean: "Can you use a better shape for the form, not
  just a mere rectangle?"
- A notch cut into each side at a dashed tear line under the proof row; the brand's ink outline and offset
  brand-colour shadow follow the shape. The notches follow the tear line when content above it changes. The side
  ticket uses the same shape. Ana: cream `#FFF8EE` card, ink outline, sunflower offset shadow, `.tkshell` / `.tkt`.
- **Draw it as ONE shape** (an SVG behind the card sized by the script), never stacked filters or masks. Ana's first
  version (five stacked drop-shadows over a mask) vanished on click in Safari and Chrome while the field glow
  animated. Sean: "the form shape, the ticket shape around the form. It glitches, like it just disappears sometimes,
  especially when I click on it." Test focus, error and typing states.
- A tiny ticket graphic belongs on every version of the form, including the side ticket (Ana: the yellow ticket icon
  in `.fl-seat`). Sean: "wheres the tiny ticket graphic here on the frozen form".
- The ticket sways once every few seconds when idle and stops while someone is in it (Ana `tksway` every 7s, off on
  `:focus-within` and with reduced motion).
- Superseded on the way (do not rebuild): a dark header bar with the logo, "Admit one" tag, 17/18/19 date tiles, a
  perforated "Seat holder" stub that filled in the name, a stamp and a barcode. Sean: "I think this form looks so
  basic." then "There's too much going on in it." Only the notch shape came back.

## 7. What goes inside the form, top to bottom

Keep it minimal: only what someone needs to sign up, but make it feel active and in demand, as if they are already in
and only have to add their name. Fewer words, not more. Sean: "Come on, you're really putting them into something.
You're not just trying to get them in. It's like they're already in, they just have to sign up." and "make it more
active and as in demand as possible".

1. **Proof row** on the ticket head: faces, five stars and a real count, then the dashed tear line. Ana `.proof`: five
   student faces, stars, "800+ student wins" (`#proofTxt`). Once real registrations pass a minimum, the count switches
   to "N people registered so far" by itself (Ana `FEED_MIN = 50`).
2. **Live pill** (only with real data): a small white pill on the ticket's top-right edge, so the left side is not
   stacked: "Maya just saved a seat · 4 min ago". Ana `.htk .tkt .just`, `top:-15px; right:22px`, 1.5px ink ring.
   Live pills always sit in front of decorations (fix the stacking order where both are defined). Sean, when the
   pill hit the fairy lights: "fix."
3. **Eyebrow row:** small accent caps with free, length and dates. Ana `.tk-k`: "Free · 3 days live · Dec 8 to 10"
   (13.5px in the hero). For visitors on other dates see section 15: their dates lead the row and are set bigger
   than the rest of it (Sean: "make date bigger here"; Ana `.tk-k.tz2 .r1 b, .ey.tz2 .r1 b` at `1.32em`).
4. **Heading that says what the form does** and names free, at a normal heading size on ONE line. Never an abstract
   tagline as the heading. Sean: "'Let's put what you know to work' is a little weird for a form" and "Can you put
   back the save your seat here?" Ana `.tk-h`: "Save your free seat", Manrope 800, 36px `nowrap` in the hero (31px
   on narrow screens, 28px in the side ticket).
   - Do not blow it up: when Sean asked for a bigger heading he meant the page H1 ("Wait, I meant the heading of the
     page"). Read which heading he means.
5. **One soft line under it** in the brand's italic accent, never replacing the action heading, never repeating it.
   Ana `.tk-and`, serif italic pink 21px: "Join me for all 3 days (for free)." (the numeral, and "(for free)" in
   brackets, each in a `nowrap` span; identical on hero, side ticket and popup). Sean: "Join me for all 3 days and add
   for free (inside parentheses)."
6. **Labels above every field,** never a bare box with placeholder text. Labels are clickable and focus their field.
   Same in the popup. Sean: "add a label on form not just a blank with placeholder. first name. email." and later
   "for the form, don't remove the first name and email label."
   - Ana: "First name" / "Email" (`.flbl`).
7. **The personal seat tag** on the right of the "First name" label: a tiny ticket and "Seat reserved for you", where
   "you" fills in with the first word they type (up to 16 characters), and drops under the label on very narrow
   phones (Ana below 360px). Must work with long names. Ana `.fl-seat` / `.fl-who`.
8. **Two fields only:** first name and email. Friendly placeholders, a small icon inside each field (person,
   envelope), a firm border. Ana: "Your first name", "The email you actually check". Sean: "I want the form to look
   more like a form". No segmentation chips in the form (Sean: "you can remove "where sre you right now" choices");
   if the copy has a segmentation question, it gets its own section and button (`registration-page.md`).
9. **The button** (section 11): "I'm in, Ana (it's free)" with the sunflower badge.
10. **Three reassurance ticks** under the button, normal case (not caps), each `nowrap`, on one line, wrapping to two
    centred lines on small phones. Ana `.fl-ticks`: "Free", "3 days live with me", "Come as you are", 12.5px.
11. **Time line, small and quiet:** the anchor time and session length. Ana `.fmeta`: "12:00 pm New York · About 90
    minutes a session". For visitors elsewhere, their own line follows (section 15).
12. **Consent note,** small, centred, balanced so no single word sits alone on the last line. Ana `.note`, 11px (the small
    lock before it was dropped when the note was centred): "You'll get emails from me, including event details and
    reminders. Unsubscribe anytime."
- The button and the ticks are the only strong things under the fields; everything else is small and quiet.
- Never inside the form: a dark logo bar, extra testimonial pills, explanatory paragraphs, session-length sentences
  beyond the time line, date tiles, stamps, stubs, barcodes, situation chips.

## 8. Field behaviour

- **A soft glow guides the eye:** the empty first-name field gets a subtle pulse in the accent on a slow loop, only
  while it is empty and not focused; once a name is in, the email field glows once; once the email looks complete, the
  button glows twice. Off with reduced motion. Never a strong light. Sean: "the first name pulse, I think we can make it
  a little bit more subtle so it won't be too much of a disturbance when they scroll to the page, because I think it's
  too strong right now." It must keep looping (it once stopped after two pulses and Sean never saw it).
  - Ana: `fhint 7s ease-in-out 2.5s infinite` (pink border `rgba(247,37,133,.75)`, 5px ring at `.12`), email
    `fhint 2.8s` once, button `bglow 2.4s` twice.
- **Email checks, in the browser and again on the server, all in one place** (one form, so one function). Clean first:
  strip spaces, a leading `mailto:`, trailing commas and full stops; lowercase the domain. Never rewrite a malformed
  address in the field. Sean: "I also want you to add criteria in the email because sometimes they're just putting the
  wrong email."
  - Hard stop, malformed (no or several @, no dot after @, ending under 2 letters, double dots, a dot next to @ or at
    the start, over 254 characters): "That doesn't look like a full email yet. Check it once more."
  - Hard stop, fake ending (.con, .cmo, .comm and similar) with a one-tap fix: "That ending isn't a real one." +
    "Did you mean maria@gmail.com? [Yes, use that]".
  - Hard stop, throwaway or placeholder inbox (mailinator, yopmail and others): "Please use an inbox you'll check.
    Temporary or example addresses won't get the Zoom link."
  - Ask once, then let it through if pressed again unchanged: near-misses of common providers (gmial.com) and short
    endings on big providers (gmail.co): "Just checking the spelling." + the "Did you mean" fix.
  - Server (Ana `api/ana-register.js`): rejects a domain with no mail server and no address ("That email's domain can't
    receive mail. Check the part after the @."), but lets the person through when the lookup is slow or unclear:
    better an occasional bad address than a blocked real person.
  - Empty first name: "add your first name".
  - **Still to do (judges, Nov 4):** in the popup the typo check lets a mistyped address through on the same click.
    A check that asks once must stop the first click and only let an unchanged address through on a second press.

### 8.1 What the form sends, and where it goes

Lock this flow before any design work (`page-sop.md` section 5, step 1). Ana's flow, as the pattern:
- **Fields sent:** first name and email, plus hidden fields added by the script: `ref` (from `?ref=`, lowercased,
  "direct" when absent), `situation` (the picker's choice: job, self or both), `sticky_variant` (the phone bar test,
  section 10), `utm_source`, `utm_medium`, `utm_campaign`, and the page address as `referrer`. A hidden honeypot field
  (`ep_check`) that only bots fill; the server answers "ok" to them and adds nobody.
- **Server first, the email tool's own form second.** The page posts to the site's own endpoint (Ana
  `/api/ana-register`), which adds the person through the email tool's API (Kit v4: the subscriber with the six fields,
  then the "Workshop registration" form), checks the email domain can receive mail, and refuses throwaway inboxes.
  Posting straight to Kit's public form address gets held by Kit's bot check, which nobody sees. Only when the
  endpoint itself fails does the page fall back to Kit's form address.
- **Someone who signs up twice still gets the welcome email:** the endpoint also puts them back into the confirmation
  sequence (Ana: `KIT_SEQUENCE_ID`, the "EP · Confirmation" sequence), because the form's automation runs only on the
  first join.
- **A live sheet of sign-ups.** Sean (Oct 31): "make the Google Sheets for the registration, so we can see in real
  time who registers." Every sign-up is also written to a "Registrants" tab (name, email, ref, the visitor's time
  zone, situation, whether it was a repeat, the UTM fields, the Kit result), best effort: it waits at most 3.5 s and
  never blocks or changes the sign-up. Keys live in Vercel (Ana: `SURVEY_SHEET_URL`, `SURVEY_SHEET_KEY`).
- **Only the client's own domains may post** (an allow list of origins on the endpoint).
- **Remember the person in the browser** (session and local storage, Ana key `ana_reg`: first name, email, ref) so the
  VIP and confirmation pages greet them by name even without the query string.
- **Then the next page:** the VIP page with `first_name`, `email` and `ref` on the address (for the greeting and the
  checkout prefill). With no form id set the page runs in demo mode: nothing is sent and it goes straight on.
- **Test without polluting the list:** nothing goes to the email tool during tests (`page-sop.md` section 8); one
  labelled test row through the live site, then tell Sean which rows to delete.

### 8.2 Saving and confirming

- **Success means confirmed.** A form or survey reports "saved" only when the receiving end confirms it wrote the row;
  read the real reply and show refusals (a wrong key) as errors. After a fix, send one labelled test row through the
  live site and tell Sean where to look and which test rows to delete. Sean: "I answered the survey, but I got nothing
  from the sheets."
- **Saved progress belongs to the email, not the browser** (surveys, unlocked tools): a different email on the same
  computer starts fresh and locked; a visit alone never overwrites saved progress. Give a reset link for testing (Ana
  `?reset=survey`). Sean: "There's an error. Why is my calculator open already? I haven't even done the survey."

## 9. Popups

**The registration popup** (Ana `#modal .dlg`):
- Same form design as the tickets, kept light: the brand mark on top, accent caps eyebrow, a short heading, one sub
  line, one live proof line, the seat tag, labelled fields, the button, the ticks, the consent note. Ana: eyebrow
  "FREE · 3 DAYS LIVE · DEC 8 TO 10", heading "Save your *free seat.*", sub "Join me for all 3 days (for free).", live
  line "800+ wins from my past students" with a green dot.
- One live line, not two; no time line and no signature inside the popup (Ana hides `.dlg .fmeta, .dlg .bye`). Sean:
  "make it a little less overwhelming because there's a lot of text going on". Never remove the field labels.
- The headline must read at a glance: no metaphor that only works in the writer's head. Sean on "Your seat is already
  pulled out.": "give me variation here what even is this". Give him numbered options and a recommendation.
- Same time and date treatment as the page forms, in the popup's own style (its capitals, its dark ink on the top
  row).
- Escape, a backdrop click and the X close it; focus stays inside and returns to the button that opened it.
- Still to do: the popup hides the time line, so a visitor outside New York sees only their dates in the eyebrow there,
  not the "For you" time line the tickets show. Ask Sean whether that line returns in the popup. The judges (Nov 4)
  also found the popup eyebrow turns all pink in time-zone mode; their dates should lead and the anchor stay small
  and grey, as on the tickets.

**The exit popup** (registration):
- Reuses the sign-up popup with an exit headline that says the seat is still theirs, plus a one-line free reminder;
  the normal headline comes back when it closes. Ana: "Don't go yet. *Your seat's still here.*" / "Put your name on it
  before you go. It's free."
- Triggers. Desktop: the mouse leaves within 24px of the top edge (heading for the tabs). Phones: a fast flick back up
  (more than 700px in under 0.5s) after reading at least 35% of the page. Never in the first 12 seconds, once per tab
  (`sessionStorage ep_exit`), never after a first name is typed or after sign-up, never when the mouse leaves through
  the side. Test hook: `?exit=1` clears the memory and cuts the wait to 2s. Sean: "Is the "Don't leave yet" actually
  working?" (it only fired at the exact top pixel; widened to 24px and tested at 0, 4 and 15px).

**VIP decline popups:** protected; see `vip-page.md` section 13. Popups use the real product screens in the page's own
finish, titles wrap cleanly. Sean: "Make it better in general. Fix the mockups used and stuff."

## 10. The phone bottom bar

- On phones the bottom bar replaces the floating header: it appears once the hero form has scrolled away and hides while
  the final section's button is on screen (Ana `#mbar`, `.mbar.on`).
- Copy: event name, dates, "Free and live on Zoom", and the same free button as the form. Ana: "The Exit Plan · Dec 8
  to 10" / "Free and live on Zoom" / "I'm in, Ana (it's free)". For visitors elsewhere the dates follow them (Ana:
  `#mbar .md` rewritten by the visitor-time script).
- It must fit from 320px with the button on one line and the arrow on screen. On the narrowest phones (389px and
  below) the event name part hides (`.mx`).
- Ana runs it as a test: half of phone visitors get the bar (`ana_sticky` cookie on/off for 90 days, sent to Kit as
  `sticky_variant`).
- Still to do:
  - below 390px Ana's bar also hides "(it's free)" (`.mbar .btn .bq{display:none}`), which conflicts with "Don't
    remove for free." Fix by tightening the bar, not by dropping the word;
  - the bar shows the visitor's dates but not their time and city. Sean: "Shouldn't the phones also have the date
    line? Isn't that important?" (in the phone pass);
  - the judges (Nov 4) found the bar overflows at 390 and 320px; fix it at both widths before adding the time;
  - whether the floating Day 1 to 3 bar moves or hides on phones is undecided.
- **Paid pages:** the bottom buy bar carries the price, the one-payment note and the same button words as the page
  (`vip-page.md` section 12). Ana VIP: "$67, one payment · I want VIP, Ana".

## 11. Buttons

**Wording**
- First person, in the visitor's voice, about what they get. Never "Join now", and never a phrase that fits another
  page's action. Sean: "also why is it "save my seat"" (on an offer page). Each placement gets its own wording, tied
  to the section's content; often addressed to the host by first name.
- Keep a long form for page buttons and a short form for the header and bars. Labels fit one line on phones.
- Ana's registration set (all open the popup):
  - header, form, bottom bar: "I'm in, Ana (it's free)";
  - hero booking card and the "who" section: "I want my exit plan, free";
  - after the days: "I'm in for all three (free)";
  - day buttons: "Show me where to start (it's free)", "Help me choose what to sell (it's free)", "Show me the path
    (it's free)";
  - host: "Show me your numbers, Ana (free)"; bring: "I'll bring mine (it's free)"; reviews: "I want to see the work
    (it's free)"; prize: "Save my seat for the draw (free)"; questions: "Questions answered. I'm in (free)";
  - gift: "Save my seat and get my number" with "your exit number comes after you register" under it;
  - fit check after the first tap: "That's me. I'm in." + "Free · 3 days live";
  - recap: "Yes, I'm coming, free"; final: "See you live, Ana!" + "Free · Live on Zoom".
- **Situation buttons:** when a section asks "where are you right now?", its button text follows the choice. Ana
  (`SITGO`): job "I want out by 2027!", self-employed "I want to get paid for what I know", both or none "I want the
  plan", with "free · live on Zoom" under it. On phones the chips come before the button.
- Offer page (Ana `/program/`, `/join/`): "Start my first paid offer", on the short checkout page with the price after
  it ("Start my first paid offer, $850 today", switching to "$1,500" on pay in full); header "Start my offer".
- Paid upsell buttons: the price in brackets on every one, never "free" (`vip-page.md` section 12). Ana VIP: "I want
  VIP, Ana ($67)".

**Say "free" on every registration button: yes.** The rule: on a free-event page, every sign-up button names free,
either in the label (a short smaller tail) or in a micro line directly under it, worded per section. The header, form
and bottom bar buttons always carry it in the label itself. Never drop it to save space.
- Why: these buttons are often seen alone (the header, the bottom bar, a section someone jumped to), and "free" is the
  word that removes the one question a cold visitor has before typing an email. It costs a few characters. Varying the
  wording keeps it from reading like a chant. Sean asked on Nov 4: "Should we say "free" on all buttons so they won't
  forget that it's free, so they will always be reminded?"; his own Oct 31 and Nov 3 copy already put free on or
  under nearly every button, and "Don't remove for free." made it a hard rule for the header.
- Set the tail smaller than the action words (Fladlien: the biggest words are the most important). Ana `.bq`:
  `font-size:.8em; font-weight:600; opacity:.85`.
- Paid buttons never say free; they show the price.

**The brand graphic on the button**
- Every main CTA carries a small custom graphic made for that client, in a round badge on the LEFT of the label. On
  hover it animates (Ana: the sunflower spins and blooms, a dashed ring turns around it, the arrow nudges); it can
  bloom in when it scrolls into view and blink when idle. With reduced motion it simply shows finished. Sean: "add a
  custom graphic that is clever and fits Ana's branding on the left side of the CTA button, something really made for
  her brand. Make it premiumly animated as well." Ana: `.sf-b` with `<use href="#sf"/>`.
- Same on every CTA on every page (registration, VIP, offer). Sean: "Can you add the sunflower logo animation on the
  CTA button? It's just like on the registration page, in the form."
- **Seasonal:** when a seasonal theme is on, every button uses the seasonal icon; count all buttons to check none are
  plain (Ana: all switch `#sf` to `#sfx`, the Santa-hat sunflower, which stays even in the toned-down Christmas layer:
  "keep the xmas sunflower on the buttons lol"). Sean: "make sure to use the new christmas themed buttons". See `../graphics.md` section 7.

**States and behaviour**
- **Never grey out a button.** Before doors open, buttons keep their colour and graphic and stay clickable; a click
  shows a short note with the opening date. Header and page buttons always share the same state. Sean: "dont grey out
  any button." Ana offer pages: "Doors open Wed Dec 9, live on Day 2."; after close "Doors are closed. Thank you."
- **Shine stays inside.** A shine or sweep runs only inside the button (`position:relative; overflow:hidden`); it once
  swept across the whole hero on phones and washed out the text. Ana uses it only on the header button and the final
  button (`.btn.shine`). Paid upsell pages: no shimmer and no pulse at all (`vip-page.md` section 12).
- **Buttons inside styled lists** keep the standard button look (accent colour, compact, centred), never the list
  item's card style. Ana's "That's me. I'm in." once showed full width and pale cream.
- **A choice row that wraps awkwardly** becomes one column of options.
- **Make hidden content findable.** If a section only opens after a click, the button is a solid accent button that
  says what they get, and a visible prompt with an arrow points at the choices until one is picked. Sean: "How do I get
  this section? I am only getting a very short one." Ana confirmation: "See my plan at $50 / $150 / $500" with "Pick a
  price to see your plan."
- **Equal options:** price or plan options are equally styled cards; never mark one best or recommended, never
  pre-select one.
- **Decline links** under paid buttons are warm, keep the free seat, wrap on small screens, and open the protected
  decline flow (`vip-page.md` section 13).
- **Test discount codes** are never applied or prefilled by a page. Sean: "The discount codes don't apply. These are
  for testing, so we can test the payment gates." (`vip-page.md` section 14).

## 12. Small cards around the CTA

- **Booking card under the hero video,** beside a slide thumbnail: a small "free, live" label, a join line that says
  free, dates, times in two zones, the button. Ana `.book`: "Free / live on Zoom", "Join The Exit Plan, free.", "Tue
  Dec 8 to Thu Dec 10", "12:00 pm New York / 7:00 pm Greece", "I want my exit plan, free". Visitors elsewhere see
  their dates and "1:00 am in Manila / 12:00 pm New York" (section 15).
- **Proof strip above the hero:** the brand line and three hard proof numbers. Ana `.tstrip`: "HOW WE GROW with Ana
  Calin" + "$1.4M from the newsletter", "About 80,000 readers", "0 sales calls".
- **Order receipt on a checkout-style offer page:** an itemised receipt read in one go: each item with "Included",
  what you leave with, payments line by line with the total, a "Due today" band, then the button. Pay in full shows one
  payment and the amount saved. Ana `/join/`: two payments of $850 ($850 today, $850 in 30 days, $1,700), pay in full
  $1,500, "You save $200". Sean: "I currently like the first part where we are showing the receipt or something".
- **Paid buy box:** the price modest, the package big, ticket tear line and notches where you pay, honest small print
  that fits inside the card. See `vip-page.md` sections 5, 10 and 11.

## 13. Tickets, badges, stickers and live signals

**Prize tickets**
- Tickets look like real printed tickets, not plain boxes: cream paper with a faint pattern, an accent stub with the
  brand mark and "ADMIT ONE", a perforated tear line, a coloured event line, the prize, a "your name?" line, the count
  and date, a small barcode. Sean: "make the tickets look better". Ana: gold stub with the sunflower, pink "THE EXIT
  PLAN · DAY 3 DRAW", "1:1 with Ana", "your name?", "ONE OF FIVE · DEC 10".
- A stack shows the full count, staggered so every ticket's body is visible, the key ticket fully in front. Art beside
  it never covers ticket text. Stamps stay small and sit on the front ticket. Sean: "You can also improve the placement
  of this and make it 5 tickets. make sure I can see the rest of the ticket body". Ana `.stay .tix`: five tickets,
  "your name?" in front, her video call ringing on a phone beside them.

**Pattern-interrupt badges** (rules in `../graphics.md` section 5; here are the UI specifics)
- A few familiar seals that pull a skimming eye to a key point: the prize, the gift, the price, the guarantee, the
  deadline. About two per page at most. Sean: "Once you slap this in somewhere, suddenly your monkey brain gets
  activated" and "Obviously, you should not overdo this".
- **Badges carry words.** Short fixed words can be lettered in Gemini; anything with a date, time or number is set on
  the page in the client's fonts. Check every letter; garbled or doubled ring text is repaired or regenerated, and the
  white background cut to transparent. Sean: "shouldnt some badges have words".
- **Never claim more than the real terms.** No "full refund", "100%", "money back guaranteed" when the refund is
  conditional; use the page's own name for the promise. Sean: "i dont wanna add full frefund". Ana program:
  "ANA'S PROMISE" / "DO THE WORK, WE FIX IT WITH YOU".
- **Placement:** on the corner of the exact thing it labels, never over a line of copy, never touching a header, never
  hanging off a box into the sticky bar; no badge where it would crowd a one-line mention. Sean: "put it properly and
  strategically and publish". They stamp in once when seen (Ana `.bdg.in`, `bdgIn .6s`).
  - Ana registration: Giveaway on the five 1:1 tickets (`.bdg-give`); Free gift beside the gift eyebrow and the first
    two heading lines (`.gift .gt-bdg`, 128px, tilted 9deg; 86px on phones, where the eyebrow takes 100px right
    padding so nothing overlaps). Sean: "you can make bonus free gift img bigger and placed smarter". VIP: Lifetime
    access on the order card corner. Program: Ana's promise on the promise box; Doors close on the calendar corner.
    Confirmation pages: none.
- **Date-aware:** a badge tied to a window hides outside it (Ana: the doors-close padlock hides before Dec 9 and after
  Dec 21; VIP seals hide after the VIP deadline).
- **Labels on page graphics:** no "Example" stamps or annotations on recreated screens. Sean: "can you remove the
  example annotation".
- **A "Most important" tag** marks the one critical step (and every step that is equally critical wears the same tag
  and shadow). Ana confirmation: WhatsApp and email both. Sean: "though the whatsapp is THE most important lol".

**Product logos and small assets**
- A tool or product gets its own small logo, not a shrunk picture of its screen. Sean: "I was thinking of a graphic
  logo of the calculator, not just how it looks, but like a logo of it, if you know what I mean." Ana: the Exit
  Number calculator badge.
- A product logo or badge Sean asks for goes in like a sticker in genuinely empty space, never over the content's text
  or numbers, checked on desktop and phone; it stamps in with the scene, then rocks gently. Sean: "Can you put the
  exit calculator logo somewhere?"
- Never copy a real brand's app icon, even tweaked; draw an original that keeps the colour association. Video call =
  a green gradient circle (light lime top to deep green bottom) with a solid white camera, no outline, matching the
  phone's green Accept button; the call screen says "Video call". Sean: "i need it green though thats he color that
  associates" and "I don't want the outline. I want it full white".

**Collaboration prints** (social proof from people the host has talked with; section spec in
`registration-page.md` section 10)
- Real frames from the host's own calls, styled like the host photo in the same section, so the row belongs there.
  Ana `.convos .cv-ph`: white mat, ink edge, yellow offset shadow, pink or yellow tape, tilted; 3:2 frames.
- Under each: the name in bold sans with the page's own video-call icon (Ana `#vcall`), then one grey credibility line.
  Sean: "use sans serif for their names", "and add a call graphic beside".
- Not clickable; no links, no play buttons, no logos of their products (logos imply a partnership). A profile photo
  badge only for a face people know at a glance (Ana: Justin Welsh, `img.cv-pfp` on his print's corner).
- 6 across on desktop, 3 on tablets, 2 on phones.

**Photo frames**
- A device frame around a client photo stays simple: a thin dark border, a slight tilt, no app chrome (no status bar,
  no Dynamic Island, no Photos app buttons). Sean: "iphone ui doesnt look realistic" and "dont use real iphone though
  i like the old size". Ana: the final section's photo in a current iPad frame (`.claim .pic .fr`, 7px dark border,
  9px on top, tilted 2.5deg).

**Stickers** (method in `../graphics.md` section 3b)
- Borders cut by hand: short straight snips, slightly crooked corners, an uneven white margin, small overcuts, a faint
  off-white edge and a soft shadow. Bridge small notches; cut out large enclosed white pockets. Sean: "can you make the
  outline more raw hand cut" and "can you cut this big white area".
- On desktop a sticker sits beside a proof card at a slight tilt, no extra frame; on phones it moves to where it covers
  nothing (Ana: right of the Google Ads card; upper right of her photo on phones, after it covered the "Sales calls"
  number). Sean: "maybe here somewhere beside the google ads".
- A sticker or rotating badge never covers headline letters; when it does, pin it in a free corner (a video corner).
- Still to do: Ana's painting sticker, leaf by leaf (Sean: "do the rest of the leaves").

**Live signals**
- **Live ticker:** simple, compact, not distracting. A thin line about 30px tall along the top edge of its section,
  taking that section's own colours, a plain pulsing dot and "live" at the left edge, small brand pennants between
  names, no avatar. Sean: "Just make it more simple and something that adjusts the look of the section." Ana
  `section > .tkb` (`top:14px; height:30px`, per-section `--tka`/`--tkb2`).
- **About three tickers on a long page:** one early, one by the reviews, one in the final section. Sean: "maybe thats a
  bit too much tickers". Check they never collide with headings or the floating bar.
- **Which ticker:** the thin pennant line above is the default. The departures board Sean first liked ("I like ticker
  B, but I want to improve and elevate the design") was simplified after "Just make it more simple and something that
  adjusts the look of the section."; it stays only as a preview (`?tk=b`).
- **The other live signals,** all from the same feed and rotating through the same real names:
  - **Pill on the hero ticket:** "Maya just saved a seat · 4 min ago" (section 7, item 2), changing name every 5 s
    with a short fade (.35 s).
  - **In the popup's proof line:** "Maya just joined" after the count line (`.fl-just`).
  - **Toast:** a small white card bottom left (20px from the edges), 1.6px ink outline, a round yellow badge with the
    first letter, "**Maya** just saved a seat" and the time ago. It slides up (.5 s), stays 4.2 s and slides away;
    first after 9 s, then every 26 s, desktop and phones. Not shown with reduced motion. `aria-live="polite"`.
- **The feed:** sign-ups from the last 3 days, first names only, the latest 8 (Ana `api/ana-feed.js`). The names show
  as soon as there is one; the count replaces the fallback at 50 (`FEED_MIN`). `?demo=1` previews everything with
  sample names; say so in any screenshot that uses it.
- Tickers, the live pill and the "just joined" toast only show with real names from the email platform. Still to do:
  the feed needs the Kit keys in the Vercel project and a redeploy; it has not shown on the live site yet.

**The host's signature** (look; the writing motion is in `motion-and-speed.md` section 5)
- A real signature, readable as her name, traced from a script font, never a line under typed text. Sean: "You
  literally just added some line underneath. I want the signature to look more like a signature, but still, her name
  should be readable." Ana: traced from the Meddon font, about 270px wide on desktop, 190px on phones
  (`min(170px,32cqw)` inside the painted frame), tilted -4deg.
- Ink in the page accent, not a colour borrowed from an outfit or a photo. Ana: navy, then red, then dusty rose were
  tried; Sean: "use the pink of the page instead" (`#F72585`, deeper `#A80F55` while wet).
- The client's wordmark sits beside it on the same line, small, with a thin divider, never under it (Sean: "looksbad,
  put it on side instad"). Ana `.hwg-cap`: gap 20px, wordmark after a 1.5px line at 15% ink.
- Balanced on the photo's mat, not hanging low: "signature should be pushed up a bit so its balanced".

## 14. The video player

- The video window is the dominant thing in the hero: shrink surrounding decoration so it covers less, no logos on the
  video, and keep the painted frame about 20px clear of the headline at every desktop width. Sean: "I just need the
  video to be a little bigger."
- Nothing sits on the play label (no name tag over it).
- The cover is a real still with a pill "tap for sound" and a pink play icon (Ana `.vplay`); tap plays with sound.
  While playing, the pill and the play bar hide (the bar shows again on hover). Ana `.iph.win.playing .vplay` and
  `.scrub`. Built on the branch; it goes live with the video.
- Measure the real window's aspect ratio before rendering a page video, and render to it (Ana's window is
  `aspect-ratio:1.548`, about 3:2, not 4:3; one edit, two renders: the window shape for desktop and 9:16 for phones,
  `video-editing.md`). Still to do: the final videos go in at publish; until then the slot shows the still.
- The host's webcam tile on screen-share slides: her full face, never cropped, a different real video frame each day,
  on the window's corner where it never covers slide content, a green speaking ring while she talks. Sean: "I want
  Anna's face screen to have some variation, like have it different each day, like a different video frame maybe, and I
  want her face to show exactly." Ana `.lv .lv-cam` (a different still per day, `.talk` adds the green ring).
- Phones: the portrait edit opens full screen in a lightbox (X, backdrop and Escape close it); when it ends, the
  lightbox closes and the page scrolls the hero form into view, since the host ends by asking for the name and email.
  Video files load only on the first tap (`preload="none"`).
- No event dates inside a page video for now. Sean: "By the way, we're not going to include the dates yet."
- Still to do: muted autoplay with captions (first lines must work without sound) and a short silent hero loop were
  planned, not built; the client's own voice for any narration, never an AI voice.

## 15. Time zones and dates

**The anchor and the visitor**
- One anchor zone for the whole funnel: the one used in emails, Zoom links, reminders and calendar invites. Ana: New
  York. Show the anchor everywhere, and the visitor's converted time beside it. Never only the visitor's time: the
  page teaches the mapping once so the anchor in later emails is familiar. Sean: "coz well have to say new york in
  emails and stuff."
- **Name the visitor's city, never "your time".** Sean: "How about instead of "your time," say "Manila" instead,
  because they might think it's not real?" Ana: "1:00 am in Manila".
- **Detect it from the device time zone** the browser reports silently (`Intl.DateTimeFormat().resolvedOptions()
  .timeZone`; city = the last segment with `_` as a space). Never ask for location (a permission popup on a sign-up
  page) and never use IP lookup (wrong on VPNs and work networks). Manchester shows "London"; accept it. Unknown,
  zone-less (no "/"), anchor-zone or same-clock values fall back to the anchor version.
- **Different day, say so.** When the visitor's date differs from the anchor date, always show the weekday and date
  with their time ("1:00 am Wed, Dec 9 in Manila") and their own event dates ("Dec 9 to 11 in Manila", highlighted).
  Same-date visitors see no extra date.
- **Times always with minutes:** "12:00 pm", never "12 pm". Change the layout, not the format. Sean: "dont remove the
  12:00 zeros. that kind of sets them more up than 12pm only."
- **Lowercase am and pm,** weekday short form in tight spots ("Tue, Dec 8"), date ranges as "Dec 8 to 10" (never a
  dash), city after the time.

- **Every date and time on the page follows the visitor,** not only the header and forms. Search the page for every
  month name, weekday and time, and make each one adapt. Sean: "fix these dates as well make them adaptable" and "and
  these. any more mention?" Visitors in the anchor zone, or with an unreadable zone, see the original page. Ana: one
  script at the end of `index.html` rewrites the date tiles, booking strip, the line under the button, the closing
  ask, the calendar invite, the thank-you line, the phone bar and the header's short date.

**Where each appears** (Ana)
| place | anchor visitor sees | visitor elsewhere sees |
|---|---|---|
| header date line | "Dec 8 to 10 · 12:00 pm New York" | their dates · time · pin + city, bold and highlighted; New York small grey under it (section 4) |
| form eyebrow | "Free · 3 days live · Dec 8 to 10" | "Free · 3 days live · **DEC 9 TO 11 IN MANILA**" (highlighted, `1.32em`) with "DEC 8 TO 10 NEW YORK" small grey directly under their dates, tight, no gap |
| form time lines | "12:00 pm New York · About 90 minutes a session" | the same, then a "For you" line with a clock icon |
| day cards | "Tuesday, Dec 8" + "12:00 pm New York" pill | their weekday, date, time and pin + city in the pill; "Tue, Dec 8 · 12:00 pm New York" beside it in grey; the calendar icon shows their date |
| booking card (`.book .d`, `.book .t`) | "Tue Dec 8 to Thu Dec 10" / "12:00 pm New York / 7:00 pm Greece" | "Wed Dec 9 to Fri Dec 11" / "**1:00 am in Manila** / 12:00 pm New York" |
| line under the hero button (`.iwhen`) | "Dec 8 to 10 · 12:00 pm New York" / "Free and live on Zoom" | "**Dec 9 to 11 · 1:00 am in Manila**" / "Free and live on Zoom" |
| closing ask (`.askt`) | "The Exit Plan · Dec 8 to 10" / "Three live sessions · About 90 minutes each · Free on Zoom" | their dates; "Three live sessions · 1:00 am in Manila · About 90 minutes each · Free on Zoom" |
| final date tiles (`.final .tiles`) | 8 Tue, 9 Wed, 10 Thu | their dates and weekdays (9 Wed, 10 Thu, 11 Fri) |
| final calendar invite (`.gi-t`) | Tuesday, December 8, 12:00 to 1:30pm, written in Google's own format (the replica keeps its dash) | their date and times, as their own calendar would show the invite |
| final times (`.ftimes`) | four cities with pins | their city on top, big and highlighted, their dates with New York's beside; the other cities small on an "Also:" line, two per row |
| thank-you line | "See you Tuesday, Dec 8." | their weekday and date |
| phone bar, header short date | anchor dates | their dates (time and city on the phone bar still to do, section 10) |

- **Form "For you" line:** their own start time on its own line, bigger and bolder than the grey note, the same soft
  highlight, with the city and always the date, and a small clock in the page's sticker style before it. Ana `.lt-me`
  13.5px bold: "For you: Wed, Dec 9 · 1:00 am in Manila" (two `nowrap` chunks), yellow clock `.lt-ic` with ink outline.
  Sean: "Also, highlight it on the forms or make it bigger or something, because time is a little bit important here."
  and "You can add a time graphic here. Yo."
- **Form eyebrow:** their dates go on the same accent row, not a new row; the anchor dates sit under THEIR dates, not
  under the start of the row, hugging with no gap. Sean: "How about if you put the December 8-10 New York under the
  December 9 instead of under the free 3 days live?" and "Stick it up to the dates on top. Don't put too much gap in
  between." Ana `.tk-k.tz2` / `.ey.tz2`, `.r1s` column with `.r2` (margin-top 0, `.88em`, grey). Keep it from looking
  like too much information.
- **Final section times:** written out per place with a small map pin on each, never abbreviations like PT or ET; at
  most four places; two columns on desktop, one centred column on phones. Sean asked "is it too much if we add more
  than 1 timezone"; the four-place list stayed because international readers do not know PT or ET or daylight time,
  and this is where people decide if they can come. Ana `.ftz`: "12:00 pm if you're in New York", "9:00 am if you're in
  Los Angeles", "5:00 pm if you're in London", "7:00 pm if you're in Greece", under "Tue Dec 8 to Thu Dec 10".
- **Once the zone is known, their city leads and the others stay small.** Sean: "how about add an area for those but
  make their city the highlighted bigger one" and "make it 2 per column instead". Pros and cons of dropping the other
  cities were discussed; Sean chose to keep them, small. Ana: their row first, highlighted (`li.me`, 19px, yellow band);
  a city not in the list gets its own row added first ("1:00 am if you're in Manila"); when their dates differ, the
  date line shows theirs with "Tue Dec 8 to Thu Dec 10 New York" beside it, grey (`.ft-d .ft-ny`, under it on phones, 640px and
  below); the other cities, New York first, fold into one grey "Also:" line (`li.ft-also`, 14px) as a grid of two
  per row with "Also:" beside them (at 380px and below, "Also:" on its own line above). Unknown zone: all four as
  before.
- **Which cities:** from where the audience lives (the email platform's location breakdown, top three or four
  countries), plus the host's home when personal. Leave out a region whose local time is unsociable (Ana: Australia,
  about 4 am Sydney). Still to do: Ana's four are a placeholder until Substack or Kit location data comes in. Sean:
  "what hshould the places be though. from her survey if there is som where they come from. the majority."
- **Where the anchor goes alone:** the form's one time line (anchor only), the header and bars (plus visitor time). The
  host's own zone appears on the booking card. The full list lives in the final section. Session length lives in the
  time line and the FAQ, not as a sentence in the form.
- **Deadlines** name weekday, date, time and city: "Mon Dec 21, 11:59 pm New York". A deadline calendar crosses off
  days by the anchor zone and outlines today.
- **When the event date moves,** move every date in the funnel by the same offset: pages, calendar files, Google
  Calendar links, paid program and welcome pages, copy that names months; ask about any date that now conflicts; after
  publish, check every live page for old dates. Sean: "can you change the dates to December 8th as day one? tuesday."

## 16. Line breaks and numerals

- **Whole phrases only.** Dates, times, city names, prices, names and short labels never split mid-phrase: "Wed, Dec
  9", "1:00 am in Manila", "Dec 9 to 11 in Kuala Lumpur", "Dec 8 to 10" each stay whole (`nowrap` spans, Ana `.nw` and
  `.nn`). Check every width down to 320px. Sean: "fix spacing looks a bit bad".
- **A dot ends a line, never starts one.** Attach the "·" to the end of the first line (Ana: "Wed, Dec 9 ·" is one
  chunk).
- **Balance short wrapped text** (`text-wrap:balance`) so no single word sits alone on the last line, and tighten line
  height on two-line notes (Ana `.lt-me` 1.5, `.r2` 1.25).
- **Headline line breaks** are hand-set phrase by phrase (`layout-type-spacing.md`).
- **Numerals in brackets:** key counts in body copy get the numeral in brackets so people see the number, kept on one
  line: Ana "three (3) free, live sessions", "two (2) copies", "two (2) hours", "seven (7) quick questions", "Five (5)
  people". Not in student quotes, buttons, headings that already use numerals, or every small "one". Sean: "make it
  three (3) just for them to visualize the number ... in the most appropriate cases". Short UI lines use the numeral
  alone: "3 days live with me", "Join me for all 3 days (for free)."

## 17. The host mascot: favicon, header icon, group pictures

One cartoon of the host, drawn in her own brand style, does several jobs: the browser tab icon, the header icon, and
the profile pictures of the free and VIP chat groups.
- **A concept, not an avatar.** Sean on the first try (polite smile, praying hands): "looks meh. pose is meh. no
  concept behind it". The pose and frame must say the brand. Ana: "Ana is the sunflower": her logo's petals bloom
  behind her head, chin on her hands like a flower. Drawn in her logo's style (thick ink outline, flat fills), with her
  real likeness (Claude writes the Gemini prompt from her real photos; Sean makes it; the client approves it, since it
  is her face).
- **One look per tier, same person:** the free version in the main brand colour; the VIP version edited from the same
  picture, in the second colour, with a status mark. Ana: yellow sunflower for every free page; pink with a crown for
  the VIP pages, a different pose for the VIP confirmation page.
- **Words on a group picture** go on a ring or banner like LinkedIn's "#Hiring" frame, designed and big enough to read
  at the small circle size ("3-day event", "VIPs"). Sean: "hmm make the text a bit btter designeed" and "and bigger
  size".
- **Where each one goes:** the free mascot is the favicon and header icon of the registration and free confirmation
  pages; the VIP mascot is the favicon and header icon of the VIP page and the VIP confirmation page. Sean: "Not that
  favicon, the one I used for the VIP confirmation page." and "make the VIP favicon the browser tab icon too."
- **Sizes:** at 16 and 32px crop tight on the face and mark so it still reads in a tab; the full picture at 180 and
  192px. A new crop or colour gets a new file name or `?v=` hash. Ana files: `img/fav/favicon*.png`, `favicon.ico`,
  `apple-touch-icon.png`, `header-ana.png` (header, web copy `img/o/fav/header-ana.webp`), and the `vip-` versions.

## 18. Still to do (Ana)

- Header fit script can drop "· A free 3-day live event" at the narrowest bar (section 2).
- Popup: decide whether the "For you" time line returns; the eyebrow turns all pink in time-zone mode; the email typo
  check lets a mistyped address through on the same click (sections 8 and 9; judges, Nov 4).
- Side form: "About 90 minutes a session" breaks across lines in the frozen ticket (section 7, item 11; judges, Nov 4).
- 320px phones: the form heading "Save your free seat" runs past the edge (section 7, item 4; judges, Nov 4).
- Phones: re-check the hero form sits under the headline, before the video (section 5).
- Phone bar: fix the overflow at 390 and 320px; keep "(it's free)" below 390px; add the visitor's time and city;
  decide the floating Day 1 to 3 bar on phones (section 10).
- Session cities from real audience data (section 15).
- Live feed: Kit keys in Vercel, then the counter, pill, tickers and toast can show (section 13).
- Final page videos at publish; muted autoplay with captions and a silent loop not built (section 14).
- Painting sticker leaves (section 13).
- VIP header CTA on phones: Sean has not said (`vip-page.md` section 4).
- Dead code: `.lt2` and `.dlt` handlers in `index.html` still write "your time"; no element uses them. Delete when
  next touched.

# The VIP (upsell) page

The page people land on right after they register for a free event: one paid upgrade, offered calmly, that the
visitor sells to themselves. This file is the standard for every client. Ana Calin's `/vip/` page (The Exit Plan,
$67) is the worked example: `2026-ana-calin/vip/index.html` plus `assets/vip-motion.js`.

Related files: `registration-page.md` (the page before this one), `ui-kit.md` (buttons, cards, headers),
`layout-type-spacing.md`, `copy.md`, `motion-and-speed.md`, `fladlien-on-pages.md`, `page-sop.md` (how a round
runs), `evolution-ana.md` (how this page got here). Playbook rules it builds on: `../graphics.md` (sections 1, 2, 3,
5, 6), `../motion.md`, `../SOP.md`, `../clients/ana-calin.md` (her facts).

## 1. Why this page is the bar

- Sean, after the Nov 1 publish: "this is fucking the most perfect VIP page we have ever built, you have ever built
  in history". He then asked to carry everything from it (graphics, animation, the Fladlien learnings, visual
  design, backgrounds, his preferences, what graphics go where, the creativity) into the registration page and
  every later page.
- What made it work, in one list:
  - one goal and nothing else: the visitor chooses VIP on their own (section 2);
  - every VIP part shown working with its real screen, never just described (section 8);
  - the free seat shown as complete and good, so VIP reads as "a little closer", never "the real version";
  - a CTA worded for every section, the price in every paid button, a warm "no thanks" under each;
  - real app copies (Gmail, Zoom Q&A, WhatsApp) the visitor can recognise at a glance;
  - the host's letter beside the price, so a person stands next to the number;
  - a calm page: flat ground, subtle section textures, nothing that pulses, real animation that tells a story;
  - the decline flow kept intact through every redesign.
- Sean on the first redesign's placements: "I liked the areas where you put the design, like the decisions are
  right. Now we have to elevate the design". Later rounds raise the look; they do not move the decisions.

## 2. The one goal

- Every section works toward one thing: the visitor picks VIP and sells it to themselves. Sean: "The goal of the
  page is to get them to sign VIP. That is the main, main, main goal ... like they would sell it to themselves.
  You're not going to sell them, and you're not going to scold them".
- No hard sell, no pressure, no scolding, no guilt in the decline. No countdown timer: the deadline is plain text.
- Do not get distracted by decoration. Before adding anything, ask: does this move them toward VIP? If not, cut it
  or quiet it.
- Judge the page honestly against `fladlien-on-pages.md` when Sean asks (he asked: "are we actually abusing Jason
  Fladlien's advice? ... Is every section helping them to work towards signing up for VIP?"). Answer with a section
  by section table: section, toward VIP yes / half / no, why.

## 3. Sections in order

| # | section | Ana's selector | job |
|---|---|---|---|
| 0 | sticky header with the pink "don't close" strip | `header.fb > .fb-card` | keep them on the page, show where they are |
| 1 | hero: saved line, spam note with inbox demo, arrow, headline, video, "what VIP adds", order card | `section.vh` | confirm the seat, make the offer once, clearly |
| 2 | your week, then free vs VIP table | `section.vw` (`.trk`, `.cmp`) | show where VIP fits in their week; compare |
| 3 | what's in VIP: one band per part, index rail | `section.vi` (`.it1` to `.it4`, `.rail-col`) | show each part working |
| 4 | pull quote, then the honest fit check | `section.vf` (`.pq`, `.fitg`) | let them qualify themselves |
| 5 | the host's letter beside the final price box, then questions | `section.vb#buy` (`.lw`, `.bb#buyBlock`, `.faqs`) | the human next to the number; answer doubts |
| 6 | footer, phone buy bar, the two decline popups | `footer`, `.mbar#mbar`, `#pop1`, `#pop2` | |

- Vary how sections open so the page is not repetitive: Ana's week and fit check open centred, the hero and items
  open left. Sean: "The UI right now is a little bit generic-ish and repetitive."
- Never let two sections share a layout (README rule 3).

## 4. Sticky header and the "don't close" strip

- One floating card, sticky 10px from the top, rounded (20px, 16px on phones), light glass
  (`rgba(255,253,249,.9)` with blur), a hairline border and a soft shadow. Never a black pill. It slims on scroll
  (`body.scrolled`: smaller padding, avatar 36px to 30px, CTA 40px to 36px). Everything fits inside the bar; nothing
  is cut. Sean: "Can you make it look a little bit nicer, because right now it looks a bit meh?" and "make it fit in
  the sticky bar as well. Make it look great."
- **The strip** (`p.keep`): a thin pink band (about 5px 14px padding, 12.5px bold white text) on top, INSIDE the
  sticky card, so it never scrolls away. Ana: "Don't close this page. Your registration isn't finished yet." with a
  small alert icon. Each phrase is `nowrap` so it wraps between phrases on phones. Sean: "No, I don't want the pink
  strip to scroll away." (An earlier version sat above the header and scrolled off; that is superseded.)
- **Left: who and what.** The VIP favicon (the illustrated host with a crown on the pink flower, the same icon as the
  VIP confirmation page), round, about 36px. Not the brand logo, not a photo. Sean: "Not that favicon, the one I
  used for the VIP confirmation page." Beside it, the free event: small caps "Free 3-day live workshop", then the
  event name in the serif with a pink date chip ("The Exit Plan" + "Dec 8 to 10"). The event name must appear on the
  page itself, not only in the tab.
  - Below 1120px the title gives way and the date chip stays; below 860px the small caps read "Free live
    workshop"; below 374px the small caps go.
- **Middle: three steps** on one thin segmented track: "Seat saved" (done, green link line) → "VIP upgrade" (now: a
  white pill with a pink number) → "Join details". Below 560px only numbers show, so nothing overlaps the date.
  - Never write "optional" on the upsell step. Sean: "On the sticky header, you don't have to put "optional."
    "Want the VIP upgrade?" Come on." The label is just the step name.
- **Right:** "STEP 2 OF 3" in small caps (hidden below 860px) and a small CTA in the brand yellow with the sunflower
  and the price: "Add VIP $67" (`.fbc`, `data-cta="header"`). Hidden below 560px because the phone buy bar holds the
  CTA within thumb reach. Still to do: Sean has not said whether he wants it on phones too.
- The browser tab icon is the VIP favicon as well (`../img/fav/vip-favicon-*.png`). Sean: "make the VIP favicon the
  browser tab icon too." Mascot rules: `ui-kit.md` section 17.
- **Page head:** title "VIP · The Exit Plan with Ana Calin", always `noindex,nofollow` (it is only for people who just
  registered), no share picture needed. Head rules: `registration-page.md` section 4.1.

## 5. Hero (`section.vh`)

In this order, centred column, then a two-column grid.

1. **Saved line + eyebrow.** A green tick and "[First name], your free seat is saved." (the name from the
   registration, if known), then a soft eyebrow: "One more thing before you go". Soft, never "One optional upgrade".
2. **The spam note with the inbox demo** (`.vspam`). Every post-registration page tells people to check Spam and
   Promotions, names the sender address, and says what they would miss. Ana's text: "**Important: check your Spam
   and Promotions folders.** Your confirmation is on its way from **anacalin@howwegrowtoday.com**. If it's there, tap
   "Not spam" or move it to your inbox, or you'll miss your Zoom link and reminders."
   - Sean's ask: "let's add a small reminder on the page after they register to also check their spam and promo
     folders and move my emails to inbox".
   - On its left, the realistic Gmail animation from the confirmation page (`.gx`, `assets/gmail-demo.css`): the
     email opens in Spam, the cursor taps "Report not spam", "In your inbox"; then the Promotions version ("Move 1
     conversation", "Conversation moved to "Primary""). The two loops take turns every 11 s. The email inside shows the
     visitor's first name. Sean: "we can add the animation that you made for that on the left side of that, so people
     would visualize".
   - Small, so it does not compete with the offer: about 690px wide, demo column 220px, 14.5px text, a white card
     with a 3px red left rule. Sean: "I want to make the spam and promotion reminder at the top be scaled down a bit
     more." Keep it at the top (Sean chose this over moving it under the order card).
3. **A pencil arrow to the offer** (`a.go-vip`, about 84px wide, 70px on phones): a hand-drawn pink line that draws
   itself like a pencil (path then head), and a tap scrolls to the video. Sean: "I want an arrow animation on there to
   make them scroll to the VIP page so it becomes the focus."
4. **Headline, A/B tested** (`#h1`). Two versions, 50/50 per visitor, kept for 90 days in a cookie; `?h=A` or
   `?h=B` previews one; the variant goes to checkout as `utm_content`. Check both versions on desktop and phone after
   every edit, and check that no variant repeats a line said under it.
   - A: "Keep the workshop for life, *and work through the hard parts with me.*"
   - B: "Get my help putting this to work, *and keep every lesson for life.*"
5. **Sub** (`.hsub`): confirm the seat, then the whole package and the price in one highlighted sentence. Ana: "You've
   saved your free seat. For $67, add lifetime workshop recordings, a live VIP Q&A and group review, private
   WhatsApp access to me during the workshop, and my Offer Clarity Sprint course."
6. **Left column: the host's video in her world.** Ana's 16:9 video sits in a painted whitewashed doorway; the pink
   door swings open on load (CSS 3D, about 1.6 s), the picture warms up from dark, petals drift. Under it: "**A minute
   with me before you decide.** Here's what VIP adds to your free seat." The video is 60 to 90 s, tap to play with
   sound. Still to do: Ana's VIP video (`VSL_SRC` is empty); it is required for launch.
7. **"What VIP adds" card** (`.hiw`) under the video: a paper card (section 11), tilted -0.4deg, a
   heading ("Use what you learn to work toward your first sales"), three lines that build one by one, each with its
   small painted icon, then the bonus line. Each line: a bold benefit, then the plain how. Ana:
   - "**Keep the teaching beside you.** Rewatch every workshop session whenever you need it, with lifetime access to
     the recordings."
   - "**Ask me while you're working on it.** Bring your questions to the private VIP WhatsApp group during the
     workshop."
   - "**See what I'd change before someone buys.** I'll review selected offers, prices and sales emails live in a
     dedicated 90-minute VIP Q&A and review."
   - then: "You also keep my Offer Clarity Sprint course. Use the part you need now, and come back to it when you're
     working on your next idea."
8. **Right column: the order card** (`aside.order#order`), a paper card tilted 0.5deg and a ticket (section 11):
   - "VIP · one payment" + "$67" small at the top; the heading "Get the full *VIP package.*" is what stands out;
   - the four parts, each with its icon, bold name then detail ("**Lifetime recordings,** all three workshop
     sessions", "**Live VIP Q&A and review** with me, 90 minutes, plus the recording", "**Private WhatsApp access** to
     me, Dec 8 to 11", "**The Offer Clarity Sprint** course, yours to keep");
   - the tear line, then "On sale until Tue, Dec 8, 11:59 pm New York" and "Total today $67.00";
   - the button "I want VIP, Ana ($67)";
   - small print: "Live review covers selected submissions." and "Secure checkout with Stripe. All sales are final."
     with a padlock. Small print must fit inside the card;
   - the decline link (section 13);
   - a "Lifetime access" seal stamped on the top corner (`.bdg-life`, tilted 11deg, 132px, 104px on phones).
   - It keeps its natural height (`align-self:start`): never stretch it to a taller left column, which leaves an
     empty gap inside.
- **On phones:** the video stays visible, and the order card sits right under the video.

## 6. Your week (`.vw`)

- Show the week as ONE object that grows across the days, with a progress line (road) through it: the free days one
  by one, the VIP session after them, then "Keep going". Sean loved this concept; it is Fladlien's storyboard device.
- Ana: one sheet of paper, painted. Day 1: the idea gets circled. Day 2: a price tag swings on. Day 3: the page folds
  into an envelope and is sealed. Friday (VIP): Ana's red pencil marks it. Keep going: it drops into a mailbox and
  letters come back.
- The outcome is "putting it in front of buyers and replies coming back". Never money, a payment notification or a
  sales number: that would promise sales.
- Day titles follow the registration page's current day titles word for word (short versions are fine in small
  timelines). Ana: "Find what you could sell and who could buy." / "Give people a reason to pay your price." / "Get
  ready to invite people to buy." then, under Thursday (not over the pictures), "Bring your work to the VIP review."
  Friday: "VIP Q&A and live review", "See what I'd improve in selected submissions." Keep going: "Put it in front of
  potential buyers and learn from the response."
- Section head: eyebrow "Your week, Dec 8 to 11", then "Work toward the sale *that makes this feel possible.*" and a
  paragraph that places VIP AFTER the free days, not instead of them: "VIP gives you the lessons to revisit and
  access to me while you put them to use."
- Colour: a white ground with one sunflower-yellow half sun rising behind Thursday to Friday (printed dot edge, pale
  rays turning very slowly, 180 s a turn). The earlier flat yellow band with grey sunflowers was replaced: Sean,
  "Not a fan of this background color ... maybe not the whole thing yellow. Maybe some shapes."
- On phones the week reads as rows: picture left, words right.

## 7. Free vs VIP table (`.cmp`)

- Title: "Your free seat and *VIP,* side by side". Columns: what you get / free seat / VIP ($67).
- Free rows first (both ticked), then the VIP rows. Ana's free rows: all three sessions live, the Day 3 prize draw
  (live attendees), live exercises, reminders on WhatsApp. VIP rows: VIP Q&A and group review, private WhatsApp
  group, the Sprint, lifetime recordings.
- The free column shows "no" for VIP-only rows, never a red cross: the free seat is not wrong.
- The VIP column is framed like a ledger column: pink header tab, thin pink side rules, a stronger pink rule at the
  bottom, a light pink tint.
- It builds row by row as it scrolls in; the VIP rows light up with their part icons.
- Under it: the CTA "Give me the VIP column ($67)", "One payment of $67, added to your free seat.", and "No thanks,
  the free seat is enough for me".
- Then one line pointing to what everyone gets next (Ana: "Free or VIP, join my WhatsApp community on the next page
  for workshop reminders. You'll also find the next steps for getting your exit number there.").

## 8. What's in VIP (`.vi`): one band per part

The pattern for every part:
- One article per part, numbered "01" to "04", alternating picture left and right (`.flip`).
- **Picture:** the part shown working as a still life on the host's table, with its real screen on a painted device:
  one main device, two props, clear margins, nothing over text. Real where proof is needed, painted where a feeling
  is (`../graphics.md` section 2). Each scene has its own short animated story (section 12).
- **Text:** number, a tag if it needs one, the headline (plain + italic half), a meta line (date · length · who), one
  paragraph with the key sentence highlighted and bold, a small labelled list ("What to bring", "When to use it",
  "When you'll want them"), an honest soft line, then the section CTA and its "no thanks".
- Paragraphs inside an item keep a gap between them.
- **Index rail** (`.rail-col`): on screens 1360px and wider, one sticky column beside the section with the four part
  icons ("Nº 01" to "Nº 04"); the current one lights up, earlier ones show done. It replaced a four-stamp strip that
  repeated over every item, which Sean called repetitive. Do not repeat the same strip over every section.
- **No "Example" stamps or captions** on recreated screens. Sean: "can you remove the example annotation". A small
  source line under a REAL screen is a different thing and is the rule (`fladlien-on-pages.md` section 2.2): Ana's
  "From the Offer Clarity Sprint" (`.src`) sits on the real course screenshot. It and the "Free, for everyone" lane
  label on the week are listed for Sean only because they are not in his Nov 1 copy (`page-sop.md` section 5.1: list
  elements not in the copy). Keep both until he says otherwise.

### 01 The live Q&A and review

- Every deliverable is its own visible feature with ONE name across the funnel (page, confirmation page, calendar
  invite). Ana's Friday session is "VIP Q&A and review" everywhere, and item 01 carries a "Live VIP Q&A" tag above
  its headline. Sean: "Where is the Q&A? ... That should be part of the features."
- Headline "Let's look at it *the way a buyer would.*"; meta "**Fri, Dec 11** · 90 minutes · VIPs only". Close the
  paragraph with the Q&A promise: "Bring your questions too: ask them in the chat and I'll answer as many as I can,
  live." Honest line: "I'll cover as many submissions as fit into 90 minutes; a personal review isn't guaranteed. You
  can submit ahead if you can't attend, and everyone gets the recording."
- **Picture:** a laptop with the review screen; a submitted sales email on paper where her red pencil strikes the
  weak line, writes "Say the price in the first line." and ticks the good one.
- **The Zoom Q&A window, copied faithfully** (`.qa`): Zoom's own blue `#0E71EB` (not the brand pink), a Mac window
  bar, "Question and Answer", the "All questions / My questions" tabs, two-letter initials, names, times, thumbs-up
  counts, "Ana Calin is answering this live" then "Answered live". The list is anchored to the bottom and scrolls up
  as questions arrive, the oldest half cut at the top. It ends with the visitor's own question typed into the box,
  sent (the count goes from 3 to 4), marked "You" and answered live.
  - Ana's questions: "Is $149 too much for my first workshop?", "Where should the price go in my email?", "What if
    nobody replies to my first email?"; the visitor types "Can I start selling before my offer is finished?".
  - Path to approval: a tilted panel with a black bar and a red LIVE badge ("The UI for the VIP queue kind of looks
    gay."), then Zoom-like in pink ("It could look more realistic."), then real Zoom in Zoom blue ("Okay, publish. You
    did amazing, sweetie.").
- CTA "Bring my offer to Friday's Q&A ($67)"; no thanks "No thanks, I'll work on my offer on my own".

### 02 The private chat (WhatsApp)

- Headline "Ask me while the question *is in front of you.*"; meta "**Dec 8 to Dec 11** · Ana in the chat".
- **The exact WhatsApp layout, themed in the client's brand and world** (`.wac`): phone status bar, the app bar in
  her pink with back arrow, the group's real VIP profile picture beside "VIP · how we grow", members ("Ana, Claire,
  Mei, Rosa, You") switching to "Ana is typing…", video, call and menu icons; a doodle wallpaper from her world
  (sunflowers, crowns, hearts, letters, coffee, price tags, pencils); the visitor's bubbles in sunflower yellow, hers
  white, time inside each bubble, tails on the first of a run, ticks that turn pink when read; the "Type a message"
  bar with emoji, clip, camera and a round yellow mic like her CTAs. Sean: "I want you to make the WhatsApp more
  realistic. Here's a picture, but I want it Anna-themed." Approved: "Beautiful, beautiful."
- The chat plays out: she opens her 30 minutes, the visitor asks, she types, she answers quoting them. Ana's script:
  "Morning, VIPs. I'm here for the next 30 minutes. Send me what you're working on" / "Quick one" / "Do I need more
  subscribers before I sell anything? I only have 212" / "No. Start with the 212 who already read you" / "Post your
  one sentence here and I'll help you tighten it" / "Posting it now. Thank you!!".
- Note the contrast: Zoom keeps Zoom's blue (realism is the point), WhatsApp wears the brand (Sean asked for it).
  Decide per app and say which.
- Beside it, the scene: a draft on the laptop, the stuck line lifting off into her phone, a voice note, three clocks
  with 30-minute wedges and a morning sun for when she is in the chat.
- State the hours plainly: "I'll be there for 30 minutes after each workshop session, plus one morning slot." Then
  separate it from the free community: "The free community has your reminders. This separate group is where we talk
  about the work."
- No caveat lines about members seeing each other's name or number. Sean asked to remove "Group members can see each
  other's phone numbers." and then "Other members can see your name and number, the way any WhatsApp group works."
- CTA "Let me ask you in the VIP chat ($67)"; no thanks "No thanks, I'll keep my questions for the live sessions".

### 03 The bonus course

- For a real product, use the real screenshot and the client's own product mockup, never a coded rebuild. Sean: "I
  want to use your actual screenshot, not this rebuilt one, and I want to use the mockup that I sent you, the full-on
  mockup." The laptop with the real lesson is the big focal piece, the mockup sits behind it (`.spr-mock`), and the
  screen zooms in on the lesson title and its key test, then the course outline, readable on a phone.
- Tease, do not give it away: show the first two of the seven stress-test questions only (an open loop); mosaic or
  blur lesson titles with dollar figures (keeps revenue claims off the page) and any private link.
- Use the course's real section names; never invent "parts".
- Headline "The Offer *Clarity Sprint.*"; meta "**Bonus** · yours to keep"; list "When to use it"; soft line "You
  don't have to finish another course before the workshop. Already own the Sprint? Bring the work you've started."
- Text drawn inside a painted card must fit with margin; if not, repaint with the text broken over lines (Ana's card:
  "I help mums go back" / "to work in six weeks."). Sean: "fix this one first, because it doesn't fit the text".
- CTA "Get the Sprint with VIP ($67)"; no thanks "No thanks, I'll skip the course".

### 04 The recordings, for life

- Headline "The workshop is yours *to keep for life.*"; meta "**Lifetime access** · all three sessions in full".
- Say a benefit literally in the copy, with a small text animation, rather than only hinting at it in a graphic.
  Ana: a white pill "Your recordings · access expires:" then "never" written in by hand in pink and underlined
  (`.exp`). On phones it is tightened so "never" does not wrap under its pill. Sean: "I want the graphic to visually
  convey that a little bit more literally. Maybe you can add it somewhere in the text as an animation".
- Picture: her week planner with "meeting ran late" slapping onto Wednesday, and a laptop replaying "DAY 2 ·
  RECORDING" with her webcam and a "saved" progress bar.
- Open with a real life moment: "A meeting runs late. You miss a session."
- CTA "Keep the workshop for life ($67)"; no thanks "No thanks, I'll catch it live".

## 9. Pull quote and honest fit check (`.vf`)

- **Pull quote:** one line from the host's own note, attached to the section it introduces (it opens the fit check
  on its pink ground, with a short pink divider after it). Never a band of its own with a big empty gap above. Sean
  pointed at the gap with "is this supposed to be like this?".
  - Ana: "That first customer matters. It gives you something to learn from, improve and sell again."
  - Byline: just the name, small pink capitals with a short line before it: ANA CALIN. No tiny photo, no "in her
    note below". Sean: "also can you change this its so funny".
- **Fit check:** eyebrow "Honest fit check", headline "Would you like me *a little closer while you do this?*".
  Both paths are good: neutral ticks on both lists, so neither looks wrong. "Get VIP if" on a paper card with a soft
  shadow; "Keep the free seat if" on a dashed, see-through card. Section opens centred, on her pink with a
  faint gingham.
  - The picture shows VIP as simply closer: a seat in the audience (`chairs-row`) vs a chair pulled up to her table.
  - The chair animation: it starts half out of frame at the card's edge, waits until the card is well in view
    (trigger at 62% of the screen), slides to the table, bumps a little closer and settles (about 1.75 s), and
    replays when you scroll back up past it. Never start it while the card is still fading in, and never let a CSS
    transition fight the GSAP tween on the same element. Sean, over three rounds: "I want this seat, this chair, to
    move faster because there's too much delay right now.", "The chair is still not moving", "where is the
    animation for the chair".
  - Under both lists, the reassurance: "**You don't need an idea or subscribers ready today.** Start with the workshop
    and bring the questions that come up."
  - CTA "Yes, pull my chair closer ($67)"; no thanks "No thanks, the free seat suits me".

## 10. The letter beside the price (`.vb#buy`)

- The host's note is a real letter beside the final price box: the person next to the number.
- Ana: a pink envelope (painted, never cut at the canvas edge: Sean, "I want you to fix this cut here"), a sunflower
  wax seal that presses on, a postmark, "A note from Ana" with her small photo, three short paragraphs,
  signed "Ana" in pink. The letter rises out of the envelope as it scrolls in.
- The body is set in the sans (Manrope 18.5px, line height 1.7; 17px on phones), not the condensed display serif. Sean: "You should
  use sans serif for this one."
- The letter says why VIP exists, in her voice, and its key sentence is highlighted: "That's what VIP is for. Keep the
  lessons, ask me about the work as you do it, and see the changes I'd make in the live review."
- **Final price box** (`.bb#buyBlock`), a ticket: "VIP" label, "$67" in the serif at 56px (not giant: the package leads), with the
  "Lifetime access" seal inside the price row; "Get the full VIP package for one payment of $67."; the same four
  parts with icons; the tear line; "Lifetime access to the workshop recordings. Support while you put the teaching
  to use."; the button "I want VIP, Ana ($67)"; "Secure checkout with Stripe. All sales are final." and "On sale until
  Tue, Dec 8 at 11:59 pm New York."; the decline link.
- **Questions** (`.faqs`) sit under the letter and price box: native `<details>` rows, the first one open ("Do I
  need VIP to come live?"), each answer starting with a plain "No." / "Yes." then the honest detail, ending with "Can
  I get a refund?" answered truthfully ("No. All sales are final. ..."). Then the button "Questions answered. Add VIP
  ($67)". Copy: `copy.md` section 10.
- **A seal inside a buy box** sits inside the box, beside the price, slightly tilted (8deg, 98px, 84px on phones),
  nothing past the box edges, its ribbon clear of the line below. Sean on the
  first try: "looks wrong". Still to do: re-measure at 1440 that the ribbon fully clears "payment of $67.".

## 11. Cards, tickets and icons

- Cards are paper, not boxes: warm white (`#FFFDF9`) on the page's warm ground (`#F8F3EB`), a hairline border
  (`rgba(26,20,18,.07)`), radius 4px, a soft three-layer lift shadow, and a tiny tilt on the hero cards (0.4 to 0.5
  degrees). No thick ink borders or hard offset shadows on this page.
- Eyebrows carry a print rule: a short hairline after the label.

- Both are styled as tickets: a dashed tear line with two round notches where you pay (`.order .tot2`, `.vb .bb
  .aside`).
- The price stays modest; the package is what stands out (Fladlien: make the most important words the biggest).
- Each VIP part has one small consistent painted icon (Ana: recording, review, chat, course: `mini-rec`, `mini-rev`,
  `mini-wa`, `mini-spr`), reused wherever the part appears (hero card, order card, table, rail, price box). Reuse
  the icon; do not repeat a whole strip over every section.

## 12. CTAs in every section

- A CTA after each major section, worded for that section, with the price in brackets on every paid button so
  checkout holds no surprise. Never "free" on a paid button. Ana's (all to the $67 checkout):
  - hero and final box: "I want VIP, Ana ($67)" (first person, to the host by first name);
  - table: "Give me the VIP column ($67)"; item 01: "Bring my offer to Friday's Q&A ($67)"; item 02: "Let me ask you
    in the VIP chat ($67)"; item 03: "Get the Sprint with VIP ($67)"; item 04: "Keep the workshop for life ($67)"; fit
    check: "Yes, pull my chair closer ($67)"; questions: "Questions answered. Add VIP ($67)";
  - header: "Add VIP $67"; phone bar: "$67, one payment" + "I want VIP, Ana".
  - Sean approved the set: "Okay, publish. You did amazing, sweetie."
- Under each section CTA: "One payment of $67, added to your free seat." and a quiet "No thanks" worded for that
  section, opening the same decline flow (Ana has seven, from "No thanks, the free seat is enough for me" to "No
  thanks, keep my free seat").
- Every button carries the brand sunflower on a cream disc on its left; on hover it spins and a dashed ring turns.
  Sean: "Can you add the sunflower logo animation on the CTA button? It's just like on the registration page".
- No shimmer, no pulse on buttons. Keep the page calm so the free seat looks complete and people pick VIP themselves.
- **Phone buy bar** (`.mbar`): fixed at the bottom on phones once the hero button has scrolled away, hidden while the
  final price box is on screen and after the deadline. Price, "one payment", and the same button words.
- **Click tracking:** every checkout link records which button sold (`data-cta` sent as `utm_term`: header, hero,
  table, qa, chat, sprint, recordings, fit, buybox, faq, mbar, pop1, pop2) plus the headline variant (`utm_content`).
- **After the deadline** (`body.is-closed`, test with `?now=2026-12-09T05:00:00Z`): every buy area reads "VIP is
  closed. *See you live.*", prices, CTAs, seals and the phone bar hide, and decline links go straight to the join
  details.

## 13. The decline flow (protected)

- The decline under the main buttons is friendly, keeps the free seat, and closes warmly with a see-you line and an
  arrow. Ana: "Coming to see what it's like? Keep your free seat. Either way, see you Tuesday →". It appears under the
  order card and under the final price box (change both). It must wrap on small screens (`white-space:normal`): a
  `nowrap` link once pushed the phone page to 588px wide.
- Every decline opens popup 1 first, never leaves directly (except after the deadline).
- **Popup 1** (`#pop1`): a pink bar with the deadline ("VIP closes Tue, Dec 8 · 11:59 pm New York"), "Wait, *before
  you go.*", "Your VIP spot for Friday, Dec 11 is still open.", a reminder the three days are free either way, the
  four parts with their real screens (not drawn mockups) under "What VIP adds to your week", "$67 one payment, added
  to the free seat you already have", the yes button "Yes, check mine on Friday ($67)", and a long first-person
  decline: "No thanks, Ana. I'll do the three days on my own and decide when I'm ready. Take me to my join details."
  - Hovering or focusing that decline turns the list red, crosses the parts out and switches the title to "What you'd
    leave behind".
  - Sean on the popup: "Make it better in general. Fix the mockups used and stuff." It now uses the real screens in
    the page's own finish (paper, hairlines), with titles that wrap cleanly.
- **Popup 2** (`#pop2`): "Are you *sure?*", the deadline and what closes ("After that, Friday's call is only for the
  people already in."), "Your free seat stays saved either way.", "No, add VIP ($67)", and "Yes, I'm sure. Take me to
  the free version." which goes to the join details (the confirmation page) with name, email and ref carried over.
- Escape, a click on the backdrop and the X close the popups; focus is trapped inside and returns to the button.
- Treat the whole flow as protected: Sean's Nov 1 copy doc said "PROTECTED DECLINE FLOW, PRESERVE THE EXISTING
  IMPLEMENTATION". Keep the trigger, both popups, the crossouts, dismissal, the routes and their wording through any
  copy update or redesign; verify line by line after each round. This is why the popups keep stronger lines the page
  itself dropped ("Your ready check, live with me", "Me, in your pocket for four days").

## 14. Checkout and after payment

- The VIP button goes straight to the client's payment link with the buyer's email prefilled and the referral id
  passed (Stripe: `prefilled_email`, `client_reference_id`). Name, email and ref come from the URL or from the
  registration stored in the browser.
- Each payment link redirects to its own page after payment, never the processor's generic thank-you page. Ana: VIP
  $67 to `/vip-confirmed/`; program paid in full to `/welcome/`; 2 payments to `/welcome/?plan=2`.
- Test coupon codes are for testing the payment gates only. The pages never apply or prefill them (Ana's
  `PROMO_CODE` stays empty). Sean: "The discount codes don't apply. These are for testing, so we can test the payment
  gates." Turn "Allow promotion codes" on in every link so the codes can be typed at checkout (Ana: ExitPlan100 for a
  $0 test, ExitPlan99 for a tiny real charge; the "Add promotion code" field sits under the price). Sean, when the
  field was missing: "still couldnt see a coupon area she said she did this". Run one $0 purchase end to end before
  launch.
- Small print near the button: the payment processor, "All sales are final" (only if true), the deadline with time
  zone, the total today, and what the review covers.
- Still to do: the VIP and regular confirmation emails, with the WhatsApp button looking attractive and required
  (Sean: "Make some buttons more attractive and required-looking, especially the WhatsApp."). Ana's VIP email is
  triggered by the Kit tag `ep_vip`.

## 15. Copy rules for this page

General copy rules are in `copy.md`. On the VIP page:
- When the client sends a full copy doc, use it word for word. After any redesign, compare every visible sentence
  with the approved copy and report that it matches. Never shorten or rewrite approved copy while redesigning; only
  additions Sean asks for (like the "don't close" strip).
- The registration page holds the newest wording. When it changes, audit the VIP page against it line by line (day
  titles, dates, times, names, the draw, session lengths, audience), list what is out of date, give an honest opinion
  of the VIP copy, and ask before changing. Then hand Sean a copyable text of the page (Ana:
  `tools/copy-vip-page.txt`).
- Never promise sales, income or a personal review for every buyer: say "selected submissions" and "a personal
  review isn't guaranteed". Sean's Nov 1 handoff: "Do not promise an individual review for every buyer." No new
  testimonials or revenue claims; carry dates over until the final schedule, never invent them.
- Explain VIP as the step after the free days, not a replacement for them.
- State the date and length of every paid session where it is sold (hero card, item, table, FAQ).
- Name each thing the same way on every page (Ana: the free "WhatsApp community" for reminders, the VIP "private
  WhatsApp group with me"), and say truthfully where a gift lives and how it is unlocked.
- A cute label ("Me, in your pocket") is used once at most, as a heading; lists and tables use the plain words.
- No jabs at the visitor (a line like "Less than the course you bought in March and never opened" was cut).
- Define a coined term the first time it appears, before it shows up in a price box.
- Never tell the same point twice on one page; when new copy goes in, reword older lines that repeat it, and check
  every A/B headline against the lines under it.
- Unclear availability wording is confirmed with the client before shipping. Still to do: Ana's "one morning slot"
  (one per day or one in total?) appears twice.
- Key lines are highlighted AND bold (`mark.sk`: a soft sunflower sweep from 52% to 94% of the line height, drawn on
  as it scrolls in), one per paragraph at most.
- Testimonials only when the client's copy includes them. Still open: Sean has not confirmed whether Gustavo's quote
  comes back.

## 16. Look

- **Background:** flat, clean and calm (white or warm white). No grain over the whole page, nothing "cheeky". Sean:
  "I still don't really like how the background looks. It looks a little cheeky".
- **Textures:** subtle, per section, made in code from Sean's references (never the references themselves, never
  solid). Sean: "use the textures and the mixins I gave to you earlier, but not in a way that it's too solid".
  Ana's: whitewash behind the door, a workbook dot grid under "What's in VIP", gingham on the pink fit check, linen
  under the letter and price, grain on the yellow footer. Cards stay clean.
- **Brand colour:** back now and then on the white base, as accents and section moods, not big flat fills. Ana: a
  soft sunshine glow behind the door, the half sun in the week, the pink fit check, a yellow footer.
- **Graphics:** painted in the client's own style (`../graphics.md` section 3, 3b), real screens on painted devices,
  balanced (one main device, two props, clear margins, nothing over text, text blocks with a set width so the text
  always fits). Sean: "Some of them are too scattered. Some of them are too tight. Make it more balanced. Sometimes
  the text doesn't fit in where they are."
- A painted asset is never cut at its canvas edge; leave room for torn edges and shadows.
- No third-party images on the live page without a licence. Ana's first redesign used Pinterest pieces; all were
  replaced by paintings made in code.
- **Seals:** one "Lifetime access" seal on the order card corner and one inside the final price row
  (`../graphics.md` section 5).

## 17. Motion

Rules are in `motion-and-speed.md` and `../motion.md`. On this page:
- Each scene acts out its own story, planned with the graphic, played once when it scrolls in (GSAP with
  ScrollTrigger, self-hosted). Ana's: the pencil marks the email and writes the note; the Zoom list fills and the
  visitor's question is answered; the chat plays message by message; the course screen zooms in; "meeting ran late"
  slaps on and the replay starts; the week's sheet folds, seals and posts; the chair slides in; the letter rises and
  the seal presses on; the door opens on the video.
- An object animation must be clearly visible: start it once its card is well in view, give it a visible travel.
- Nothing pulses or nags. Reduced motion shows every scene finished.
- Decoration that sells nothing is a candidate to cut (Claude's audit named the rising sun and the drifting petals;
  Sean kept them).

## 18. Checks after every round

- Every visible sentence against the approved copy (a script diff against the last commit).
- Both popups, the hover crossouts, Escape, the checkout link (email prefilled, `utm_term`, `utm_content`), both
  headline variants, the closed state (`?now=`), the phone buy bar.
- No sideways scroll and no script errors at 320, 390, 1024 and 1440.
- Header at every breakpoint: nothing overlaps or is cut.
- Text inside every card and painted graphic fits; seals clear their neighbours.
- Send screenshots (or a motion recording) section by section; publish only on Sean's word, then check the live page.

## 19. Adapting it to another client

1. Copy the section order (section 3). Keep the one goal and the protected decline flow from day one.
2. List the client's VIP parts. Give each one name used across the whole funnel, one small icon in their style, a
   date and length, and an honest limit (who gets reviewed, when they are in the chat).
3. For each part decide real or painted (`../graphics.md` section 2) and find the real screen: their review tool,
   their chat app, their course, their recordings. Copy real apps exactly; theme them in the brand only where Sean
   asks (Ana: WhatsApp in brand, Zoom in Zoom blue).
4. Pick the week object from their world (Ana: a sheet of paper that becomes a letter) and the fit check metaphor
   for "a little closer" (Ana: a chair pulled up to her table).
5. Write CTAs in the buyer's first person to the host by first name, price in brackets, one per section, each with
   its own "no thanks".
6. Build the header: the strip in their accent, their VIP favicon, the free event name and dates, the three steps.
7. Wire the checkout: payment link, email prefill, ref, `data-cta` tracking, the after-payment redirect, promotion
   codes on, a $0 test.
8. Put their letter beside the price, in the sans, with their own seal or mark.
8b. Photos of the client are her own (or stills from her recordings), in simple frames with no app chrome; proof
   from people she has talked with is real frames and checked lines, never logos (`registration-page.md` sections 10
   and 24).
9. Run the checks (section 18) and the Fladlien review (`fladlien-on-pages.md`).

## 20. Still to do (Ana)

- The VIP video (`VSL_SRC` empty), required for launch.
- A cleaner Sprint mockup: the client's AI-made one has garbled text ("Fraineworks Sotty") and odd figures
  ("1 Customer = $11,988", "Lifetime Value $11,788"). Flag AI artefacts in client mockups and ask for a clean version.
- The Fladlien gaps Claude listed and Sean has not answered: named proof near the item it proves (Jill Hart's note),
  a price anchor (the Sprint's normal price), a reason for the price, risk reversal (a guarantee is Ana's call), "All
  sales are final" as the last words under the button.
- "One morning slot" wording; whether the header CTA shows on phones; the leftover "Free, for everyone" and "From the
  Offer Clarity Sprint" labels; Gustavo's testimonial; the Offer Clarity link on the VIP confirmation page (Sean: "On
  the VIP, I think."); the confirmation emails; the seal ribbon at 1440.
- Open: since Nov 4 every date and time on the registration page follows the visitor (`ui-kit.md` section 15). The
  VIP page still shows New York only (the bar's "Dec 8 to 10", "See you Tue Dec 8." in the Gmail demo, "On sale until
  Tue, Dec 8, 11:59 pm New York"). Ask Sean whether the VIP page follows too; a deadline keeps New York beside the
  visitor's time.
- The footer's "help" link is Sean's own address as a placeholder (`mailto:sean@theafterharvest.com`; the code notes
  the guide still had "[sean@theafterharvest.com or the launch alias]"). Ask Sean for the launch help address before
  launch.
